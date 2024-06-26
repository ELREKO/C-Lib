# handle_s

## Description

The function **size_t handle_s(int fd, va_list args)** handles the conversion specifier `%s` in formatted output. It retrieves a string argument from the argument list `args` and writes it to the file descriptor `fd`.

## Declaration

```c
size_t handle_s(int fd, va_list args);
```

## Parameters

- **fd**: File descriptor where the output will be written.
- **args**: Argument list containing the string to be written.

## Return Value

- Returns the number of characters written to `fd`.

## Example

```c
#include "lib_main.h"

int main() {
    char *str = "Hello, World!";
    ft_printf("Output string: %s\n", str); // Output will be "Hello, World!"
    return 0;
}
```

## Usage

1. **String Output**: Writes the string argument to the specified file descriptor.
2. **Null Pointer Handling**: If the string pointer is `NULL`, outputs `"(null)"`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
