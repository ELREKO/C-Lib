# ft_putchar_fd

## Description

The function **void ft_putchar_fd(char c, int fd)** writes the character **c** to the file descriptor **fd**.

## Declaration
```c
void ft_putchar_fd(char c, int fd);
```
## Parameters

- **c**: The character to be written.
- **fd**: The file descriptor to which the character will be written.

## Return Value

This function does not return a value.

## Example
```c
#include "lib_main.h"

int main() {
    char c = 'A';
    int fd = 1; // Standard output

    ft_putchar_fd(c, fd);

    return 0;
}
```
## Usage

1. **Character Writing**: The function writes the character **c** to the specified file descriptor **fd** using the `write` system call.
2. **Simple I/O**: It is useful for low-level character output operations, particularly when working with custom file descriptors.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
