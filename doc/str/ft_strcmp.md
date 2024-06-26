# ft_strcmp

## Description

The function **int ft_strcmp(const char *s1, const char *s2)** compares the string `s1` and the string `s2`. It compares the characters of both strings and returns an integer based on the comparison.

## Declaration

```c
int ft_strcmp(const char *s1, const char *s2);
```

## Parameters

- **s1**: The first string to be compared (`const char *`).
- **s2**: The second string to be compared (`const char *`).

## Return Value

- Returns an integer less than, equal to, or greater than zero if `s1` is found, respectively, to be less than, to match, or be greater than `s2`.
- Returns `1` if either `s1` or `s2` is `NULL`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "Hello";
    const char *str2 = "Hello";
    
    int result = ft_strcmp(str1, str2);
    
    if (result == 0) {
        printf("Strings are equal.\n");
    } else if (result < 0) {
        printf("String s1 is less than s2.\n");
    } else {
        printf("String s1 is greater than s2.\n");
    }
    
    return 0;
}
```

## Usage

1. **String Comparison**: Compares the characters of `s1` and `s2` until a null terminator is reached or a difference is found.
2. **Return Values**: Returns `0` if `s1` is equal to `s2`, a negative value if `s1` is less than `s2`, and a positive value if `s1` is greater than `s2`.
3. **Null Handling**: Returns `1` if either `s1` or `s2` is `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
