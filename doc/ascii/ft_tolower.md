# ft_tolower

## Description

The function **int ft_tolower(int c)** converts the argument **c** to lowercase if it is an uppercase letter.

The `ft_tolower` function checks if the character `c` is an uppercase letter ('A' to 'Z'). If `c` is within this range, it converts it to its corresponding lowercase letter by adding 32 to its ASCII value.

## Declaration
```c
int ft_tolower(int c);
```
## Parameters

- **c**: The character to be converted, provided as an integer.

## Return Value

This function returns the lowercase equivalent of the character `c` if `c` is an uppercase letter. If `c` is not an uppercase letter, it returns `c` unchanged.

## Example
```c
#include "lib_main.h"

int main() {
    char uppercase = 'C';
    char lowercase = ft_tolower(uppercase);
    printf("Uppercase: %c, Lowercase: %c\n", uppercase, lowercase); // Output will be "Uppercase: C, Lowercase: c"
    return 0;
}
```
### Usage

1. **Character Checking**: The function checks if the character `c` is an uppercase letter.
2. **Conversion**: If `c` is an uppercase letter, it converts it to lowercase using ASCII manipulation.
3. **Return Value**: It returns the lowercase equivalent of `c` if `c` is an uppercase letter, or `c` unchanged if not.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
