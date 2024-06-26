# ft_strncmp

## Description

The function **int ft_strncmp(const char *s1, const char *s2, size_t n)** compares at most `n` characters of the null-terminated strings `s1` and `s2`. It compares the characters in the two strings and returns an integer based on their lexicographical comparison.

## Declaration

```c
int ft_strncmp(const char *s1, const char *s2, size_t n);
```

## Parameters

- **s1**: Pointer to the null-terminated first string to compare (`const char *`).
- **s2**: Pointer to the null-terminated second string to compare (`const char *`).
- **n**: Number of characters to compare (`size_t`).

## Return Value

- Returns an integer less than, equal to, or greater than zero if the first `n` characters of `s1` are found, respectively, to be less than, to match, or be greater than the first `n` characters of `s2`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "hello";
    const char *str2 = "world";
    int cmp1 = ft_strncmp(str1, str2, 3); // Compare first 3 characters
    int cmp2 = ft_strncmp(str1, str2, 5); // Compare first 5 characters

    printf("Comparison 1 (first 3 characters): %d\n", cmp1);
    printf("Comparison 2 (first 5 characters): %d\n", cmp2);

    return 0;
}
```

## Usage

1. **String Comparison**: Compares the first `n` characters of strings `s1` and `s2`.
2. **Lexicographical Order**: Determines the lexicographical order of the compared characters.
3. **Return Value**: Returns an integer based on the comparison result:
   - Negative value if `s1` is less than `s2`.
   - Zero if `s1` is equal to `s2` up to `n` characters.
   - Positive value if `s1` is greater than `s2`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
