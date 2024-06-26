# ft_isdigit

## Description

The function **int ft_isdigit(int c)** checks whether the argument **c** is a digit character ('0' to '9').

The `ft_isdigit` function determines if the character `c` falls within the range of digit characters.

## Declaration
```c
int ft_isdigit(int c);
```
## Parameters

- **c**: The character to be checked, provided as an integer.

## Return Value

This function returns 1 if the character is a digit ('0' to '9'), and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = '5';
    if (ft_isdigit(character)) {
        printf("%c is a digit.\n", character); // Output will be "5 is a digit."
    } else {
        printf("%c is not a digit.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Range Checking**: The function checks if the character `c` falls within the range of '0' to '9'.
2. **Return Value**: It returns 1 if `c` is a digit character, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
