# ft_isalnum

## Description

The function **int ft_isalnum(int c)** checks whether the argument **c** is an alphanumeric character (i.e., a letter or a digit).

The `ft_isalnum` function determines if the character `c` falls within the range of alphanumeric characters, which includes lowercase letters ('a' to 'z'), uppercase letters ('A' to 'Z'), and digits ('0' to '9').

## Declaration
```c
int ft_isalnum(int c);
```
## Parameters

- **c**: The character to be checked, provided as an integer.

## Return Value

This function returns 1 if the character is alphanumeric, and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = '7';
    if (ft_isalnum(character)) {
        printf("%c is alphanumeric.\n", character); // Output will be "7 is alphanumeric."
    } else {
        printf("%c is not alphanumeric.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Range Checking**: The function checks if the character `c` falls within the ranges of lowercase letters, uppercase letters, or digits.
2. **Return Value**: It returns 1 if `c` is alphanumeric, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
