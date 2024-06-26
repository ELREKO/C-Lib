# ft_strjoin

## Description

The function **char *ft_strjoin(char const *s1, char const *s2)** concatenates two strings `s1` and `s2` into a newly allocated string.

## Declaration

```c
char *ft_strjoin(char const *s1, char const *s2);
```

## Parameters

- **s1**: The first string (`char const *`).
- **s2**: The second string (`char const *`).

## Return Value

- Returns a pointer to a newly allocated string that contains the concatenation of `s1` followed by `s2`. If memory allocation fails, returns `NULL`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *s1 = "Hello";
    char *s2 = "World";
    char *result = ft_strjoin(s1, s2);

    if (result) {
        printf("Concatenated string: %s\n", result);
        free(result); // Don't forget to free the allocated memory
    } else {
        printf("Memory allocation failed.\n");
    }

    return 0;
}
```

## Usage

1. **Concatenation**: Concatenates the strings `s1` and `s2`.
2. **Memory Allocation**: Allocates memory dynamically for the result string.
3. **Return Value**: Returns `NULL` if memory allocation fails.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
