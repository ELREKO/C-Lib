# free_char_variadic_code

## Description

The function **int free_char_variadic_code(int code, int num, ...)** frees dynamically allocated memory for multiple `char *` variables passed as variable arguments (`...`). It takes an integer `code` and the number of `char *` arguments (`num`). Each `char *` argument is assumed to point to dynamically allocated memory that needs to be freed using `free()`.

## Declaration

```c
int free_char_variadic_code(int code, int num, ...);
```

## Parameters

- **code**: Integer code to be returned after freeing memory.
- **num**: Number of `char *` arguments passed as variable arguments (`...`).
- **...**: Variable number of `char *` arguments, each pointing to memory that needs to be freed.

## Return Value

Returns the provided `code` after successfully freeing all `char *` arguments. If `num` is `0` or less, it returns `0` without performing any operations.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *str1 = malloc(sizeof(char) * 10);
    char *str2 = malloc(sizeof(char) * 20);
    
    // Assume str1 and str2 are allocated and used
    
    int result = free_char_variadic_code(0, 2, str1, str2);
    if (result != 0) {
        perror("Error freeing memory");
        return -1;
    }
    
    return 0;
}
```

## Usage

1. **Memory Deallocation**: It iterates through each `char *` argument and frees the dynamically allocated memory using `free()`.
2. **Return Code**: It returns the provided `code` after successfully freeing all memory. If no memory was freed (when `num` is `0` or less), it returns `0` to indicate success.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
