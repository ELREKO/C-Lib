# ft_toupper

## Description

The function **int ft_toupper(int c)** converts the argument **c** to uppercase if it is a lowercase letter.

The `ft_toupper` function checks if the character `c` is a lowercase letter ('a' to 'z'). If `c` is within this range, it converts it to its corresponding uppercase letter by subtracting 32 from its ASCII value.

## Declaration
```c
int ft_toupper(int c);
```
## Parameters

- **c**: The character to be converted, provided as an integer.

## Return Value

This function returns the uppercase equivalent of the character `c` if `c` is a lowercase letter. If `c` is not a lowercase letter, it returns `c` unchanged.

## Example
```c
#include "lib_main.h"

int main() {
    char lowercase = 'b';
    char uppercase = ft_toupper(lowercase);
    printf("Lowercase: %c, Uppercase: %c\n", lowercase, uppercase); // Output will be "Lowercase: b, Uppercase: B"
    return 0;
}
```
### Usage

1. **Character Checking**: The function checks if the character `c` is a lowercase letter.
2. **Conversion**: If `c` is a lowercase letter, it converts it to uppercase using ASCII manipulation.
3. **Return Value**: It returns the uppercase equivalent of `c` if `c` is a lowercase letter, or `c` unchanged if not.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
