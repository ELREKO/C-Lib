# ft_putnbr_base_fd_ul

## Description

The function **size_t ft_putnbr_base_fd_ul(int fd, unsigned long nbr, const char *base)** writes an unsigned long integer to the specified file descriptor using the given numeral system (base).

The `ft_putnbr_base_fd_ul` function converts an unsigned long integer to its string representation in a specified base and writes it to a file descriptor. It uses helper functions to manage the conversion and writing process.

## Declaration

size_t ft_putnbr_base_fd_ul(int fd, unsigned long nbr, const char *base);

## Parameters

- **fd**: The file descriptor to which the number will be written.
- **nbr**: The unsigned long integer to be converted and written.
- **base**: A pointer to a string representing the base to use for conversion.

## Return Value

This function returns the number of characters written to the file descriptor.

## Example

```c
#include "lib_main.h"

int main() {
    int fd = 1; // Standard output
    unsigned long number = 255;
    const char *base = "0123456789ABCDEF"; // Hexadecimal base

    size_t chars_written = ft_putnbr_base_fd_ul(fd, number, base);
    printf("\nCharacters written: %zu\n", chars_written); // Output will be "FF\nCharacters written: 2"

    return 0;
}
```

## Internal Functions

### put_character_ul

```c
static void put_character_ul(int fd, unsigned long nbr, t_base_info base_info, size_t *chars_printed);
```

The `put_character_ul` function handles the recursive conversion and writing of the number to the file descriptor.

### ft_putnbr_base_check

```c
size_t ft_putnbr_base_check(const char *base, t_base_info *base_info);
```

The `ft_putnbr_base_check` function validates the provided base string and updates the `base_info` structure.

### ft_putchar_fd_len

```c
size_t ft_putchar_fd_len(char c, int fd);
```

The `ft_putchar_fd_len` function writes a character to the specified file descriptor and returns the number of characters written.

## Usage

1. **Base Validation**: The function first checks if the provided base is valid using `ft_putnbr_base_check`.
2. **Recursive Conversion**: It uses `put_character_ul` to recursively convert the number to the specified base and write it to the file descriptor.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
