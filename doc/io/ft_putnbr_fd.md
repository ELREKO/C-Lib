# ft_putnbr_fd

## Description

The function **void ft_putnbr_fd(int n, int fd)** writes the integer **n** to the specified file descriptor **fd**. It handles both positive and negative numbers, including the edge case of the minimum integer value.

## Declaration

```c
void ft_putnbr_fd(int n, int fd);
```

## Parameters

- **n**: The integer to be written to the file descriptor.
- **fd**: The file descriptor to which the number will be written.

## Example

```c
#include "lib_main.h"

int main() {
    int fd = 1; // Standard output
    int number = -12345;

    ft_putnbr_fd(number, fd);
    // Output will be: -12345

    return 0;
}
```

## Internal Functions

### ft_putchar_fd

```c
void ft_putchar_fd(char c, int fd);
```

The `ft_putchar_fd` function writes a character to the specified file descriptor.

### Usage

1. **Handle Minimum Integer Value**: The function first checks if **n** is equal to **INT_MIN**. If so, it handles this edge case separately since **INT_MIN** cannot be negated without overflow.
2. **Handle Negative Numbers**: If **n** is negative, the function writes a '-' character to the file descriptor and negates **n**.
3. **Recursive Conversion**: The function uses recursion to break down the integer and write each digit to the file descriptor.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
