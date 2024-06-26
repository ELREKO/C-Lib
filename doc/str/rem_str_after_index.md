# rem_str_after_index

## Description

The function **int rem_str_after_index(char **res, t_ins_repl_str replace_info)** removes the substring after a specified index in the original string `replace_info.org_str`. It modifies `*res` to contain the resulting string. Returns 0 on success, or an error code otherwise.

## Declaration

```c
int rem_str_after_index(char **res, t_ins_repl_str replace_info);
```

## Parameters

- **res**: Pointer to a pointer that will store the resulting string (`char **`).
- **replace_info**: Structure containing information needed for string removal (`t_ins_repl_str`).

### Structure `t_ins_repl_str`

```c
typedef struct	s_ins_repl_str
{
	char	*org_str;               // Original string
	char	*repl_str;              // String to find and replace
	char	*ins_str;               // String to insert
	int		search_start_index;     // Start index for searching in org_str
}				t_ins_repl_str;
```

- **org_str**: Original string from which the substring will be removed.
- **repl_str**: String to find in `org_str` and remove everything after.
- **ins_str**: Not used in this context (only relevant for insertion).
- **search_start_index**: Index in `org_str` to start searching for `repl_str`.

## Return Value

- Returns 0 on success.
- Returns 1 if `org_str` is NULL.
- Returns 2 if memory allocation fails during duplication of `org_str`.
- Returns 3 if `repl_str` is not found in `org_str`.
- Returns 4 if memory allocation fails during string joining.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *result = NULL;
    t_ins_repl_str replace_info = {
        .org_str = "Hello world, remove this part.",
        .repl_str = "remove this part",
        .ins_str = "",
        .search_start_index = 0
    };

    int status = rem_str_after_index(&result, replace_info);

    if (status == 0) {
        printf("Original string: \"%s\"\n", replace_info.org_str);
        printf("Resulting string: \"%s\"\n", result);
        free(result);
    } else {
        printf("Error occurred: %d\n", status);
    }

    return 0;
}
```

## Usage

1. **String Removal**: Searches for `repl_str` in `org_str` starting from `search_start_index` and removes everything after `repl_str`.
2. **Memory Management**: Handles memory allocation internally; returns appropriate error codes on failure.
3. **Error Handling**: Checks for NULL pointers and ensures valid operations based on `replace_info`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
