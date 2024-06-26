# ft_vdprintf

## Description

The function **int ft_vdprintf(int fd, const char *format, va_list args)** writes formatted output to the specified file descriptor `fd`, based on the format string `format` and the variable argument list `args`.

The `ft_vdprintf` function is similar to `vdprintf` and processes the format string `format`, identifying and handling format specifiers prefixed by `%`. It delegates the formatting tasks to specific handler functions (`handle_c`, `handle_s`, `handle_p`, `handle_d_i`, `handle_u`, `handle_x`, `handle_cap_x`, and `%`), which interpret and format the corresponding data types (`char`, `string`, `pointer`, `integer`, `unsigned integer`, `hexadecimal`, `uppercase hexadecimal`, and `%`). If a specifier is not recognized, it writes the character directly to the file descriptor.

## Declaration

```c
int ft_vdprintf(int fd, const char *format, va_list args);
```

## Parameters

- **fd**: The file descriptor where the formatted output is written.
- **format**: The format string that contains format specifiers and text.
- **args**: The variable argument list that provides the data to be formatted according to the format string.

## Return Value

This function returns the total number of characters written to the file descriptor `fd`. On error, it returns `-1`.

## Example

```c
#include "lib_main.h"
#include <stdarg.h>
#include <stdio.h>

int main() {
    int fd = 1; // stdout
    const char *format = "This is a formatted output: %s %d\n";
    int num = 10;
    const char *str = "hello";
    
    int result = ft_vdprintf(fd, format, num, str);
    printf("Total characters written: %d\n", result); // Output will vary based on implementation
    return 0;
}
```

## Internal Functions

### handle_specifiers

```c
static void handle_specifiers(int fd, const char *cur_format, ssize_t *spec_chars_written, va_list args);
```

The `handle_specifiers` function processes each format specifier in the format string and delegates the corresponding formatting task to specialized handler functions.

### Usage

1. **Initialization**: The function initializes variables to track the total number of characters written (`tot_write_count`).
2. **Format String Processing**: It iterates through each character in the format string.
3. **Specifier Handling**: For each `%` character encountered, it calls `handle_specifiers` to process the specifier and format the corresponding data.
4. **Error Handling**: If an unrecognized specifier is encountered (`*spec_chars_written = -2`), it handles it accordingly.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
