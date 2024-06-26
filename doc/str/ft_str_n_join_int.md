# ft_str_n_join_int

## Description

The function **int ft_str_n_join_int(const char *s1, const char *s2, int n, char **res)** joins up to `n` characters from `s2` onto the end of `s1` and allocates memory for the result in `res`. If `n` is `0`, it concatenates the entire string `s2`. If either `s1` or `s2` is `NULL`, it duplicates the non-NULL string directly into `res`.

## Declaration

```c
int ft_str_n_join_int(const char *s1, const char *s2, int n, char **res);
```

## Parameters

- **s1**: The null-terminated string to which `s2` will be joined (`const char *`).
- **s2**: The null-terminated string to be joined onto `s1` (`const char *`).
- **n**: The maximum number of characters from `s2` to concatenate onto `s1` (`int`).
- **res**: A pointer to a pointer where the resulting joined string will be stored (`char **`).

## Return Value

- Returns `1` on success.
- Returns `-1` if memory allocation fails.
- The resulting joined string is stored in `*res`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *s1 = "Hello, ";
    const char *s2 = "world!";
    char *joined_string = NULL;
    
    int status = ft_str_n_join_int(s1, s2, 0, &joined_string);
    
    if (status == 1 && joined_string) {
        printf("Joined string: %s\n", joined_string);
        free(joined_string);
    } else {
        printf("Joining failed or memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **String Concatenation**: Concatenates up to `n` characters from `s2` onto `s1`.
2. **Memory Allocation**: Allocates memory for `*res` to store the resulting joined string.
3. **Handling `n` Values**: If `n` is `0`, concatenates the entire string `s2` onto `s1`.
4. **Null Checks**: If either `s1` or `s2` is `NULL`, duplicates the non-NULL string directly into `res`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
