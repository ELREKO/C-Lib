# ft_isalpha

## Description

The function **int ft_isalpha(int c)** checks whether the argument **c** is an alphabetic character (i.e., a letter).

The `ft_isalpha` function determines if the character `c` falls within the range of alphabetic characters, which includes lowercase letters ('a' to 'z') and uppercase letters ('A' to 'Z').

## Declaration
```c
int ft_isalpha(int c);
```
## Parameters

- **c**: The character to be checked, provided as an integer.

## Return Value

This function returns 1 if the character is an alphabetic character, and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = 'B';
    if (ft_isalpha(character)) {
        printf("%c is an alphabetic character.\n", character); // Output will be "B is an alphabetic character."
    } else {
        printf("%c is not an alphabetic character.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Range Checking**: The function checks if the character `c` falls within the ranges of lowercase letters or uppercase letters.
2. **Return Value**: It returns 1 if `c` is an alphabetic character, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
