# ft_putendl_fd

## Description

The function **void ft_putendl_fd(char *s, int fd)** writes the string **s** to the file descriptor **fd**, followed by a newline character.

## Declaration
```c
void ft_putendl_fd(char *s, int fd);
```
## Parameters

- **s**: The null-terminated string to be written.
- **fd**: The file descriptor to which the string will be written.

## Return Value

This function does not return a value.

## Example
```c
#include "lib_main.h"

int main() {
    char *str = "Hello, World!";
    int fd = 1; // Standard output

    ft_putendl_fd(str, fd);

    return 0;
}
```
## Usage

1. **String Writing**: The function writes the string **s** to the specified file descriptor **fd** using the `ft_putstr_fd` function.
2. **Newline Addition**: It appends a newline character after the string using the `ft_putchar_fd` function.
3. **Simple I/O**: Useful for writing strings with a newline in one function call, especially when working with custom file descriptors.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
