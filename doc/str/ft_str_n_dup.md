# ft_str_n_dup

## Description

The function **char *ft_str_n_dup(const char *s, int n)** duplicates up to `n` characters from the string `s` into a newly allocated string `new_str`. If `n` is `0`, it copies the entire string `s`. The function allocates memory for `new_str` based on the size of `n` characters plus one for the null terminator.

## Declaration

```c
char *ft_str_n_dup(const char *s, int n);
```

## Parameters

- **s**: The null-terminated string to be duplicated (`const char *`).
- **n**: The maximum number of characters to duplicate (`int`).

## Return Value

- Returns a pointer to the newly allocated duplicated string on success.
- Returns `NULL` if memory allocation fails or if `s` is `NULL`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *s = "Hello, world!";
    char *duplicate = ft_str_n_dup(s, 5);
    
    if (duplicate) {
        printf("Duplicated substring: %s\n", duplicate);
        free(duplicate);
    } else {
        printf("Memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **Substring Duplication**: Duplicates up to `n` characters from `s` into `new_str`.
2. **Memory Allocation**: Allocates memory for `new_str` based on the size of `n` characters plus one for the null terminator.
3. **Handling `n` Values**: If `n` is `0`, duplicates the entire string `s`.
4. **Null Terminator**: Ensures the duplicated string is null-terminated.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
