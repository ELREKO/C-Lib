# ft_itoa

## Description

The function **char *ft_itoa(int n)** converts the integer argument **n** to a null-terminated string representing the integer value.

The `ft_itoa` function converts an integer to an ASCII string. It handles negative numbers by adding a `-` sign at the beginning of the string. The function allocates memory for the resulting string, which must be freed by the caller to avoid memory leaks.

## Declaration
```c
char *ft_itoa(int n);
```

## Parameters

- **n**: The integer to be converted.

## Return Value

This function returns a pointer to the null-terminated string representing the integer value. If the memory allocation fails, it returns `NULL`.

## Example
```c
#include "lib_main.h"

int main() {
    int number = -12345;
    char *result = ft_itoa(number);
    if (result) {
        printf("Converted string: %s\n", result); // Output will be "-12345"
        free(result);
    }
    return 0;
}
```
## Internal Functions

### get_num_digs

static size_t get_num_digs(long n_l);

The `get_num_digs` function calculates the number of digits in the number, ignoring the sign.

### Usage

1. **Initialization**: The function initializes variables for the result (`res`) and the length of the string.
2. **Sign Handling**: It checks if the number is negative and adjusts the length accordingly.
3. **Memory Allocation**: It allocates memory for the resulting string.
4. **Number Conversion**: It converts the integer into an ASCII string.
5. **Return**: It returns the resulting string.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
