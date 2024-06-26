# ft_atoi_secure

## Description

The function **int ft_atoi_secure(const char *nptr)** converts the string argument **nptr** to an integer (type int) with additional checks to handle overflow and underflow.

The `ft_atoi_secure` function converts an ASCII string to a (signed) integer. It skips all whitespace characters until the first non-whitespace character is found. A `+` or `-` sign can precede the number to indicate its sign. The function includes checks to handle too many digits and ensure that the resulting value does not exceed the range of an `int`. If any character in the string cannot be converted, the conversion stops, and the number interpreted so far is returned.

## Declaration
```c
int ft_atoi_secure(const char *nptr);
```
## Parameters

- **nptr**: A pointer to the null-terminated string to be converted.

## Return Value

This function returns the converted integral number as an `int` value. If the converted value exceeds the `int` range, it returns `INT_MAX` or `INT_MIN`.

## Example

#include "lib_main.h"
```c
int main() {
    const char *number = "2147483648"; // One more than INT_MAX
    int result = ft_atoi_secure(number);
    printf("Converted number: %d\n", result); // Output will be INT_MAX
    return 0;
}
```
## Internal Functions

### handle_to_many_dig

static int handle_to_many_dig(const char *nptr, int sign, long *res);

The `handle_to_many_dig` function checks if the string has too many digits and sets the result to `INT_MAX` or `INT_MIN` accordingly.

### ft_strlen_1_to_9

static int ft_strlen_1_to_9(const char *int_str);

The `ft_strlen_1_to_9` function calculates the length of the string ignoring leading zeros and returns the length of the number part.

### Usage

1. **Initialization**: The function initializes variables for the result (`res`) and the sign of the number.
2. **Whitespace Skipping**: It skips over any whitespace characters at the beginning of the string.
3. **Sign Handling**: It checks for a `+` or `-` sign to determine the sign of the resulting number.
4. **Digit Length Check**: It checks if the number has too many digits to fit into an `int`.
5. **Number Conversion**: It converts the string into an integer.
6. **Overflow Handling**: It ensures the result does not exceed `INT_MAX` or `INT_MIN`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
