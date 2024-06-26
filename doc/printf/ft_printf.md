# ft_printf

## Description

The function **int ft_printf(const char *format, ...)** prints formatted output to the standard output. It accepts a variable argument list similar to the standard C `printf` function and internally uses `ft_vdprintf` to output the formatted data.

## Declaration

```c
int ft_printf(const char *format, ...);
```

## Parameters

- **format**: A pointer to a null-terminated string containing format specifiers and text to be formatted.
- **...**: Variable argument list containing values to be interpreted according to the format specifiers in `format`.

## Return Value

- Returns the number of characters successfully outputted, or -1 on error.

### Example

```c
#include "lib_main.h"

int main() {
    ft_printf("Hello, %s! You are %d years old.\n", "John", 30);
    return 0;
}
```

## Usage

1. **Formatted Output**: Functions similar to `printf`, but uses `ft_vdprintf` for output.
2. **Variable Argument List**: Allows formatting and outputting various data types like strings, numbers, and characters.

---

## ft_printf_fd

### Description

The function **int ft_printf_fd(int fd, const char *format, ...)** prints formatted output to a specified file descriptor `fd`. It works similarly to `ft_printf` but allows outputting to a specific file descriptor.

### Declaration

```c
int ft_printf_fd(int fd, const char *format, ...);
```

### Parameters

- **fd**: The file descriptor to which the formatted data should be written.
- **format**: A pointer to a null-terminated string containing format specifiers and text to be formatted.
- **...**: Variable argument list containing values to be interpreted according to the format specifiers in `format`.

### Return Value

- Returns the number of characters successfully outputted, or -1 on error.

### Example

```c
#include "lib_main.h"

int main() {
    int fd = open("output.txt", O_WRONLY | O_CREAT, 0644);
    ft_printf_fd(fd, "This is written to a file descriptor!\n");
    close(fd);
    return 0;
}
```

### Usage

1. **File Descriptor**: Allows outputting formatted data to a specific file descriptor.
2. **Flexible Formatting**: Can be used like `printf` to output data with different format specifiers to different file descriptors.

---

## ft_printf_to_str

### Description

The function **int ft_printf_to_str(char **res, const char *format, ...)** returns formatted output as a dynamically allocated string. It internally uses a pipe mechanism to collect the output and returns the resulting string via `res`.

### Declaration

```c
int ft_printf_to_str(char **res, const char *format, ...);
```

### Parameters

- **res**: A pointer to a pointer to a null-terminated string. This is where the resulting formatted string is returned.
- **format**: A pointer to a null-terminated string containing format specifiers and text to be formatted.
- **...**: Variable argument list containing values to be interpreted according to the format specifiers in `format`.

### Return Value

- Returns the number of characters successfully outputted, or -1 on error.

### Example

```c
#include "lib_main.h"

int main() {
    char *result = NULL;
    int chars_printed = ft_printf_to_str(&result, "Formatted string: %s, Number: %d\n", "Hello", 123);
    if (chars_printed != -1) {
        printf("Result: %s\n", result);
        free(result);
    } else {
        printf("Error in ft_printf_to_str\n");
    }
    return 0;
}
```

### Usage

1. **Dynamic String**: Stores formatted output in a dynamically allocated string returned via `res`.
2. **Pipe Mechanism**: Uses a pipe to collect output and convert it into a string.

---

# Summary

These `printf`-like functions offer flexibility for different use cases: outputting to the standard output, a specific file descriptor, or a dynamically allocated string. They enable formatting and outputting of data according to the specified format specifiers in the input string `format`.

If you have further questions or wish to describe other functions, please let me know!

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)