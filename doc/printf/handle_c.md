# handle_c

## Description

The function **size_t handle_c(int fd, va_list args)** handles the conversion specifier `%c` in formatted output. It retrieves a character argument from the argument list `args` and writes it to the file descriptor `fd`.

## Declaration

```c
size_t handle_c(int fd, va_list args);
```

## Parameters

- **fd**: File descriptor where the character will be written.
- **args**: Argument list containing the character to be formatted.

## Return Value

- Returns the number of characters written to `fd`.

## Example

```c
#include "lib_main.h"

int main() {
    char ch = 'A';
    ft_printf("Character: %c\n", ch); // Example output: "Character: A"
    return 0;
}
```

## Usage

1. **Character Output**: Writes the character specified by `%c` to the file descriptor `fd`.
2. **Unicode Characters**: Handles characters including special and non-printable characters as required.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
