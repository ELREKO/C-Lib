# ft_str_n_dup_int

## Description

The function **int ft_str_n_dup_int(const char *s, int n, char **res)** copies up to `n` characters from the string `s` into a newly allocated string `res`. If `n` is less than or equal to `0`, it copies the entire string `s`. The function allocates memory for `res` based on the size of `n` characters plus one for the null terminator.

## Declaration

```c
int ft_str_n_dup_int(const char *s, int n, char **res);
```

## Parameters

- **s**: The null-terminated string to be copied (`const char *`).
- **n**: The maximum number of characters to copy (`int`).
- **res**: A pointer to a pointer where the result will be stored (`char **`).

## Return Value

- Returns `1` on success.
- Returns `-1` if memory allocation fails.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *s = "Hello, world!";
    char *res = NULL;
    
    if (ft_str_n_dup_int(s, 5, &res) == 1) {
        printf("Copied substring: %s\n", res);
        free(res);
    } else {
        printf("Memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **Substring Copying**: Copies up to `n` characters from `s` into `res`.
2. **Memory Allocation**: Allocates memory for `res` based on the size of `n` characters plus one for the null terminator.
3. **Handling `n` Values**: If `n` is less than or equal to `0`, copies the entire string `s`.
4. **Null Terminator**: Ensures the copied string is null-terminated.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
