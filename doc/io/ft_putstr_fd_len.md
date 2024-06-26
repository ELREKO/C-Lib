# ft_putstr_fd_len

## Description

The function **size_t ft_putstr_fd_len(char *s, int fd)** writes a null-terminated string **s** to the specified file descriptor **fd**. It counts and returns the number of characters written to the file descriptor.

## Declaration

```c
size_t ft_putstr_fd_len(char *s, int fd);
```

## Parameters

- **s**: The null-terminated string to be written to the file descriptor.
- **fd**: The file descriptor to which the string will be written.

## Return Value

This function returns the number of characters written to the file descriptor.

## Example

```c
#include "lib_main.h"

int main() {
    int fd = 1; // Standard output
    char *message = "Hello, world!\n";
    size_t printed_chars = ft_putstr_fd_len(message, fd);
    // Output (on screen): Hello, world!
    // printed_chars will be: 14

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
3. **Counting**: The function counts and returns the total number of characters written.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
