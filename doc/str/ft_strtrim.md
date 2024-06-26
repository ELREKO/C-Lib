# ft_strtrim

## Description

The function **char *ft_strtrim(char const *s1, char const *set)** trims leading and trailing characters from the string `s1` that match any character in the null-terminated string `set`. Returns a newly allocated string that is a trimmed copy of `s1`, without the specified leading and trailing characters.

## Declaration

```c
char *ft_strtrim(char const *s1, char const *set);
```

## Parameters

- **s1**: Pointer to the null-terminated string to trim (`const char *`).
- **set**: Pointer to the null-terminated string containing the characters to trim (`const char *`).

## Return Value

- Returns a newly allocated string that is a trimmed copy of `s1`, or `NULL` if memory allocation fails or if `s1` or `set` are NULL.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "   Hello, world!   ";
    const char *set = " ";
    char *trimmed_str = ft_strtrim(str, set);

    if (trimmed_str) {
        printf("Original string: \"%s\"\n", str);
        printf("Trimmed string: \"%s\"\n", trimmed_str);
        free(trimmed_str);
    } else {
        printf("Memory allocation failed.\n");
    }

    return 0;
}
```

## Usage

1. **Trimming Characters**: Removes leading and trailing characters from `s1` that match any character in `set`.
2. **Null Termination**: Ensures the returned string is null-terminated.
3. **Memory Allocation**: Handles memory allocation internally; returns `NULL` on failure.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
