# ft_str_cont_chars

## Description

The function **int ft_str_cont_chars(const char *str, const char *set)** checks if any character from the string `str` is present in the set of characters `set`. It returns `1` if at least one character from `str` is found in `set`, otherwise it returns `0`.

## Declaration

```c
int ft_str_cont_chars(const char *str, const char *set);
```

## Parameters

- **str**: The null-terminated string to be checked (`const char *`).
- **set**: The set of characters to search for (`const char *`).

## Return Value

- Returns `1` if any character from `str` is found in `set`.
- Returns `0` if none of the characters from `str` are found in `set`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "Hello, world!";
    const char *set = "aeiou";
    
    if (ft_str_cont_chars(str, set)) {
        printf("String '%s' contains at least one vowel from set '%s'.\n", str, set);
    } else {
        printf("String '%s' does not contain any vowels from set '%s'.\n", str, set);
    }
    return 0;
}
```

## Usage

1. **Character Search**: The function checks each character in `str` to see if it exists in the `set`.
2. **Return Value**: Returns `1` upon finding a match, otherwise `0`.
3. **Set of Characters**: Specifies the characters in `set` against which `str` characters are compared.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
