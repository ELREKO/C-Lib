# free_char_variadic_msg

## Description

The function **int free_char_variadic_msg(char *msg, int num, ...)** frees dynamically allocated memory for multiple `char *` variables passed as variable arguments (`...`). Additionally, it prints a formatted message (`msg`) using `ft_printf` after freeing the memory. It takes an integer `num` to specify the number of `char *` arguments, and each `char *` argument is assumed to point to dynamically allocated memory that needs to be freed using `free()`.

## Declaration

```c
int free_char_variadic_msg(char *msg, int num, ...);
```

## Parameters

- **msg**: Message to be printed after freeing memory.
- **num**: Number of `char *` arguments passed as variable arguments (`...`).
- **...**: Variable number of `char *` arguments, each pointing to memory that needs to be freed.

## Return Value

Returns the return value of `ft_printf`, which prints the formatted `msg` to the standard output. If `num` is `0` or less, it returns `0` without performing any memory freeing or printing.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *str1 = malloc(sizeof(char) * 10);
    char *str2 = malloc(sizeof(char) * 20);
    
    // Assume str1 and str2 are allocated and used
    
    int result = free_char_variadic_msg("Memory freed successfully", 2, str1, str2);
    if (result <= 0) {
        perror("Error printing message");
        return -1;
    }
    
    return 0;
}
```

## Usage

1. **Memory Deallocation**: It iterates through each `char *` argument and frees the dynamically allocated memory using `free()`.
2. **Message Printing**: It prints the formatted `msg` using `ft_printf` after successfully freeing all memory.
3. **Return Code**: It returns the return value of `ft_printf`, which indicates the success or failure of printing the message.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
