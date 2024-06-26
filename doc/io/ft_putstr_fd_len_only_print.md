# ft_putstr_fd_len_only_print

## Description

The function **size_t ft_putstr_fd_len_only_print(char *s, int fd)** writes a string **s** to the specified file descriptor **fd**, skipping non-printable characters. It counts and returns the number of printable characters written to the file descriptor.

## Declaration

```c
size_t ft_putstr_fd_len_only_print(char *s, int fd);
```

## Parameters

- **s**: The null-terminated string to be written to the file descriptor.
- **fd**: The file descriptor to which the string will be written.

## Return Value

This function returns the number of printable characters written to the file descriptor.

## Example

```c
#include "lib_main.h"

int main() {
    int fd = 1; // Standard output
    char *message = "Hello!\nThis is a test.\n";
    size_t printed_chars = ft_putstr_fd_len_only_print(message, fd);
    // Output (on screen): Hello!This is a test.
    // printed_chars will be: 18

    return 0;
}
```

## Internal Functions

### ft_isprint

```c
int ft_isprint(int c);
```

The `ft_isprint` function checks whether the given character **c** is a printable character as defined by the ASCII character set.

### ft_putchar_fd_len

```c
size_t ft_putchar_fd_len(char c, int fd);
```

The `ft_putchar_fd_len` function writes a single character **c** to the specified file descriptor **fd** and returns the number of bytes written.

### Usage

1. **Character Validation**: The function iterates through each character in the string **s**.
2. **Printable Character Check**: It checks if each character is printable using the `ft_isprint` function.
3. **Output**: If a character is printable, it is written to the file descriptor using `ft_putchar_fd_len`.
4. **Counting**: The function counts and returns the number of printable characters written.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
