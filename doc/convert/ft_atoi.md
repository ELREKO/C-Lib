# ft_atoi

## Description

The function **int ft_atoi(const char *nptr)** converts the string argument **nptr** to an integer (type int).

The `ft_atoi` function converts an ASCII string to a (signed) integer. It skips all whitespace characters until the first non-whitespace character is found. A `+` or `-` sign can precede the number to indicate its sign. If any character in the string cannot be converted, the conversion stops, and the number interpreted so far is returned.

## Declaration
```c
int ft_atoi(const char *nptr);
```
## Parameters

- **nptr**: A pointer to the null-terminated string to be converted.

## Return Value

This function returns the converted integral number as an `int` value. If no valid conversion could be performed, it returns zero.

## Example
```c
#include "lib_main.h"

int main() {
    const char *number = "   -12345";
    int result = ft_atoi(number);
    printf("Converted number: %d\n", result); // Output will be -12345
    return 0;
}
```
### Usage

1. **Initialization**: The function initializes variables for the result (`res`) and the sign of the number.
2. **Whitespace Skipping**: It skips over any whitespace characters at the beginning of the string.
3. **Sign Handling**: It checks for a `+` or `-` sign to determine the sign of the resulting number.
4. **Number Conversion**: It converts the string into an integer.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
