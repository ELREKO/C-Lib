# ft_atoi_base_l

## Description

The function **ssize_t ft_atoi_base_l(const char *nptr, const char *base)** converts the string argument **nptr** to a long integer based on the provided numeral system (base).

The `ft_atoi_base_l` function converts an ASCII string to a (signed) long integer according to the specified base. It first checks if the base is valid using `ft_putnbr_base_check`. Then, it skips all whitespace characters until the first non-whitespace character is found. A `+` or `-` sign can precede the number to indicate its sign. If any character in the string cannot be converted, the conversion stops, and the number interpreted so far is returned.

## Declaration
```c
ssize_t ft_atoi_base_l(const char *nptr, const char *base);
```
## Parameters

- **nptr**: A pointer to the null-terminated string to be converted.
- **base**: A pointer to a string representing the base to use for conversion.

## Return Value

This function returns the converted integral number as a `ssize_t` value. If no valid conversion could be performed, it returns zero.

## Example
```c
#include "lib_main.h"

int main() {
    const char *number = "1010";
    const char *base = "01"; // Binary base
    ssize_t result = ft_atoi_base_l(number, base);
    printf("Converted number: %ld\n", result); // Output will be 10
    return 0;
}
```
## Internal Functions

### get_res

static void get_res(const char *nptr, t_base_info base_info, long *res);

The `get_res` function processes the string to compute the resulting number based on the base.

### Usage

1. **Initialization**: The function initializes variables for the result (`res`) and the sign of the number.
2. **Base Validation**: It checks if the provided base is valid.
3. **Whitespace Skipping**: It skips over any whitespace characters at the beginning of the string.
4. **Sign Handling**: It checks for a `+` or `-` sign to determine the sign of the resulting number.
5. **Number Conversion**: It converts the string into a long integer based on the provided base.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
