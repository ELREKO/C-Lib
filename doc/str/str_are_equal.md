# str_are_equal

## Description

The function **int str_are_equal(const char *s1, const char *s2)** compares two strings `s1` and `s2` to check if they are equal. It returns 1 if they are equal (including the case where both are NULL), and 0 otherwise.

## Declaration

```c
int str_are_equal(const char *s1, const char *s2);
```

## Parameters

- **s1**: Pointer to the first string (`const char *`).
- **s2**: Pointer to the second string (`const char *`).

## Return Value

- Returns 1 if `s1` and `s2` are equal (including both being NULL).
- Returns 0 if `s1` and `s2` are not equal.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "Hello";
    const char *str2 = "Hello";
    const char *str3 = "World";

    printf("str1 and str2 are equal: %d\n", str_are_equal(str1, str2));
    printf("str1 and str3 are equal: %d\n", str_are_equal(str1, str3));
    printf("str2 and str3 are equal: %d\n", str_are_equal(str2, str3));
    printf("NULL and NULL are equal: %d\n", str_are_equal(NULL, NULL));

    return 0;
}
```

## Usage

1. **String Comparison**: Performs character-by-character comparison until a difference is found or both strings terminate.
2. **Handling NULL Pointers**: Returns 1 if both `s1` and `s2` are NULL.
3. **Comparison Result**: Returns 0 if `s1` and `s2` differ or if one of them is NULL while the other is not.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
