# handle_p

## Description

The function **size_t handle_p(int fd, va_list args)** handles the conversion specifier `%p` in formatted output. It retrieves a pointer argument from the argument list `args` and writes its hexadecimal representation prefixed with `0x` to the file descriptor `fd`.

## Declaration

```c
size_t handle_p(int fd, va_list args);
```

## Parameters

- **fd**: File descriptor where the output will be written.
- **args**: Argument list containing the pointer to be formatted.

## Return Value

- Returns the number of characters written to `fd`.

## Example

```c
#include "lib_main.h"

int main() {
    void *ptr = malloc(sizeof(int));
    ft_printf("Pointer address: %p\n", ptr); // Example output: "Pointer address: 0x7ffee3a39960"
    free(ptr);
    return 0;
}
```

## Usage

1. **Pointer Output**: Converts the pointer argument to its hexadecimal representation.
2. **Null Pointer Handling**: If the pointer is `NULL`, outputs `"(nil)"`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
