# handle_cap_x

## Description

The function **size_t handle_cap_x(int fd, va_list args)** handles the conversion specifier `%X` in formatted output. It retrieves an unsigned integer argument from the argument list `args` and writes its hexadecimal representation (uppercase) to the file descriptor `fd`.

## Declaration

```c
size_t handle_cap_x(int fd, va_list args);
```

## Parameters

- **fd**: File descriptor where the output will be written.
- **args**: Argument list containing the unsigned integer to be formatted.

## Return Value

- Returns the number of characters written to `fd`.

## Example

```c
#include "lib_main.h"

int main() {
    unsigned int num = 255;
    ft_printf("Hexadecimal value: %X\n", num); // Example output: "Hexadecimal value: FF"
    return 0;
}
```

## Usage

1. **Hexadecimal Output**: Converts the unsigned integer argument to its hexadecimal representation using uppercase letters (`A-F`).
2. **Zero Padding**: Handles zero-padding as necessary to maintain format consistency.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
