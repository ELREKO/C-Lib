# ft_strrchr

## Description

The function **char *ft_strrchr(const char *s, int c)** locates the last occurrence of the character `c` (converted to a char) in the string `s`. The terminating null byte ('\0') is considered part of the string. Returns a pointer to the located character or `NULL` if the character does not appear in the string.

## Declaration

```c
char *ft_strrchr(const char *s, int c);
```

## Parameters

- **s**: Pointer to the null-terminated string to search within (`const char *`).
- **c**: Character to search for (converted to `unsigned char`).

## Return Value

- Returns a pointer to the last occurrence of `c` in the string `s`, or `NULL` if `c` does not appear in the string.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "Hello, world! This is a test string.";
    int ch = 'l';
    char *result = ft_strrchr(str, ch);

    if (result)
        printf("Last occurrence of '%c' found at position: %ld\n", ch, result - str);
    else
        printf("Character '%c' not found in the string.\n", ch);

    return 0;
}
```

## Usage

1. **Character Search**: Searches for the last occurrence of `c` in `s`.
2. **Terminating Null**: Considers the terminating null byte ('\0') as part of the string.
3. **Return Value**: Returns a pointer to the located character or `NULL` if `c` is not found in `s`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
