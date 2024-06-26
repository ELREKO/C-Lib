# ft_putchar_fd_len

## Description

The function **size_t ft_putchar_fd_len(char c, int fd)** writes the character **c** to the file descriptor **fd** and returns the number of bytes written.

## Declaration
```c
size_t ft_putchar_fd_len(char c, int fd);
```

## Parameters

- **c**: The character to be written.
- **fd**: The file descriptor to which the character will be written.

## Return Value

This function returns the number of bytes written, which should be 1.

## Example
```c
#include "lib_main.h"

int main() {
    char c = 'A';
    int fd = 1; // Standard output

    size_t bytes_written = ft_putchar_fd_len(c, fd);
    printf("Bytes written: %zu\n", bytes_written); // Output will be 1

    return 0;
}
```
## Usage

1. **Character Writing**: The function writes the character **c** to the specified file descriptor **fd** using the `write` system call.
2. **Return Value**: It returns the number of bytes written, which helps in verifying the success of the write operation.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
