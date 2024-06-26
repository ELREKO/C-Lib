
# ft_bzero

## Description

The function **void *ft_bzero(void *s, size_t n)** sets the first **n** bytes of the memory area pointed to by **s** to zero.

## Declaration

```c
void *ft_bzero(void *s, size_t n);
```

## Parameters

- **s**: Pointer to the memory area to be zeroed.
- **n**: Number of bytes to be zeroed starting from **s**.

## Return Value

- The function returns a pointer to the memory area **s**.

## Example

```c
#include "lib_main.h"

int main() {
    char buffer[10] = "Hello";
    
    ft_bzero(buffer, 5);
    
    ft_printf("Buffer after bzero: %s\n", buffer); // Output will be "     "
    
    return 0;
}
```

## Usage

1. **Zeroing Memory**: The function is used to clear a specified number of bytes in memory starting from the address **s**.
2. **Setting Bytes to Zero**: It sets each byte to zero ('\0').

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
