# ft_join_n_str

## Description

The function **int ft_join_n_str(char **res, int num, ...)** joins a variable number of strings (`num` strings) together into a single dynamically allocated string (`res`). It uses the function `ft_str_n_join_int` to perform the joining operation and manages memory allocation for the resulting string.

## Declaration

```c
int ft_join_n_str(char **res, int num, ...);
```

## Parameters

- **res**: A pointer to a pointer to a string (`char **`) where the joined string will be stored.
- **num**: An integer specifying the number of strings to join.
- **...**: Variable number of arguments (`char *`) representing the strings to be joined.

## Return Value

- Returns `1` if the operation is successful.
- Returns `-1` if memory allocation fails during the join operation.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *result = NULL;
    int num_strings = 3;

    int status = ft_join_n_str(&result, num_strings, "Hello", ", ", "world", "!");
    if (status == 1) {
        printf("Joined string: %s\n", result);
        free(result); // Free the dynamically allocated string
    } else {
        printf("Error: Join operation failed.\n");
    }

    return 0;
}
```

## Usage

1. **Joining Strings**: The function joins `num` strings provided as variadic arguments (`...`) into a single dynamically allocated string (`res`).
2. **Memory Management**: It uses `ft_str_n_join_int` for joining and manages memory allocation for the resulting string.
3. **Error Handling**: Returns `-1` if memory allocation fails during the join operation.

---

# free_va_arg

## Description

The static function **static int free_va_arg(va_list args, int code)** frees the `va_list` `args` and returns the provided `code`.

## Declaration

```c
static int free_va_arg(va_list args, int code);
```

## Parameters

- **args**: `va_list` variable to be freed.
- **code**: Integer code to be returned by the function.

## Return Value

- Returns the provided `code`.
- Frees the `va_list` `args`.

## Usage

1. **Freeing `va_list`**: The function frees the `va_list` `args` and returns the provided `code`.
2. **Memory Management**: Ensures proper cleanup of `va_list` resources.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
