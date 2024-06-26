# ft_isascii

## Description

The function **int ft_isascii(int c)** checks whether the argument **c** is a 7-bit ASCII character.

The `ft_isascii` function determines if the character `c` falls within the range of 7-bit ASCII characters, which are values from 0 to 127 (inclusive).

## Declaration
```c
int ft_isascii(int c);
```
## Parameters

- **c**: The character to be checked, provided as an integer.

## Return Value

This function returns 1 if the character is a 7-bit ASCII character, and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = '!';
    if (ft_isascii(character)) {
        printf("%c is a 7-bit ASCII character.\n", character); // Output will be "! is a 7-bit ASCII character."
    } else {
        printf("%c is not a 7-bit ASCII character.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Range Checking**: The function checks if the character `c` falls within the range of 7-bit ASCII characters (0 to 127).
2. **Return Value**: It returns 1 if `c` is a 7-bit ASCII character, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
