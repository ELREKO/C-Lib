# ft_putstr_fd

## Description

The function **void ft_putstr_fd(char *s, int fd)** writes a null-terminated string **s** to the specified file descriptor **fd**.

## Declaration

```c
void ft_putstr_fd(char *s, int fd);
```

## Parameters

- **s**: The null-terminated string to be written to the file descriptor.
- **fd**: The file descriptor to which the string will be written.

## Return Value

This function does not return a value.

## Example

```c
#include "lib_main.h"

int main() {
    int fd = 1; // Standard output
    char *message = "Hello, world!\n";
    ft_putstr_fd(message, fd);
    // Output (on screen): Hello, world!

    return 0;
}
```

## Internal Functions

### ft_putchar_fd

```c
void ft_putchar_fd(char c, int fd);
```

The `ft_putchar_fd` function writes a single character **c** to the specified file descriptor **fd**.

### Usage

1. **Character Output**: The function iterates through each character in the string **s**.
2. **Output**: Each character is written to the file descriptor **fd** using the `ft_putchar_fd` function.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
