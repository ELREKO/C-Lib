# ft_isspace

## Description

The function **int ft_isspace(char c)** checks whether the argument **c** is a whitespace character.

The `ft_isspace` function determines if the character `c` is a whitespace character according to the ASCII standard. Whitespace characters include space (' '), newline ('\n'), vertical tab ('\v'), horizontal tab ('\t'), form feed ('\f'), and carriage return ('\r').

## Declaration
```c
int ft_isspace(char c);
```
## Parameters

- **c**: The character to be checked, provided as a character.

## Return Value

This function returns 1 if the character `c` is a whitespace character, and 0 otherwise.

## Example
```c
#include "lib_main.h"

int main() {
    char character = '\t';
    if (ft_isspace(character)) {
        printf("%c is a whitespace character.\n", character); // Output will be "\t is a whitespace character."
    } else {
        printf("%c is not a whitespace character.\n", character);
    }
    return 0;
}
```
### Usage

1. **Character Checking**: The function checks if the character `c` matches any of the whitespace characters defined by the ASCII standard.
2. **Return Value**: It returns 1 if `c` is a whitespace character, and 0 otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
