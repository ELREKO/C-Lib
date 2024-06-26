# ft_isprint

## Description

The function **int ft_isprint(int c)** checks whether the argument **c** is a printable character (including space) in the ASCII character set.

The `ft_isprint` function determines if the character `c` falls within the range of printable ASCII characters, which are values from 32 to 126 (inclusive).

## Declaration
```c
int ft_isprint(int c);
```
## Parameters

- **c**: The character to be checked, provided as an integer.

## Return Value

This function returns 1 if the character is a printable ASCII character, and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = '#';
    if (ft_isprint(character)) {
        printf("%c is a printable character.\n", character); // Output will be "# is a printable character."
    } else {
        printf("%c is not a printable character.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Range Checking**: The function checks if the character `c` falls within the range of printable ASCII characters (32 to 126).
2. **Return Value**: It returns 1 if `c` is a printable character, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
