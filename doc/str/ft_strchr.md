# ft_strchr

## Description

The function **char *ft_strchr(const char *s, int c)** locates the first occurrence of the character `c` (converted to a `char`) in the string `s`. It returns a pointer to the located character, or `NULL` if the character `c` does not appear in the string `s`.

## Declaration

```c
char *ft_strchr(const char *s, int c);
```

## Parameters

- **s**: The null-terminated string to be searched (`const char *`).
- **c**: The character to search for (`int`), which is treated as an unsigned char for the comparison.

## Return Value

- Returns a pointer to the first occurrence of the character `c` in the string `s`.
- Returns `NULL` if the character `c` is not found in the string `s`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "Hello, world!";
    char *found_char = NULL;
    int search_char = 'o'; // Character to search for
    
    found_char = ft_strchr(str, search_char);
    
    if (found_char) {
        printf("First occurrence of '%c' found at position: %ld\n", search_char, found_char - str);
    } else {
        printf("Character '%c' not found in the string.\n", search_char);
    }
    
    return 0;
}
```

## Usage

1. **Character Search**: Finds the first occurrence of the character `c` in the string `s`.
2. **Pointer Return**: Returns a pointer to the located character or `NULL` if `c` is not found.
3. **Comparison**: Treats `c` as an unsigned char for comparison with characters in `s`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
