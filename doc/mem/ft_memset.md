# ft_memset

## Description

The function **void *ft_memset(void *s, int c, size_t n)** fills the first **n** bytes of the memory area pointed to by **s** with the constant byte **c**.

## Declaration

```c
void *ft_memset(void *s, int c, size_t n);
```

## Parameters

- **s**: Pointer to the memory area to be filled.
- **c**: Value to be set. The value is converted to an `unsigned char` before being stored.
- **n**: Number of bytes to be set to the value **c**.

## Return Value

- Returns a pointer to the memory area **s**.

## Example

```c
#include "lib_main.h"

int main() {
    char buffer[10] = {0};

    ft_memset(buffer, 'A', 5); // Fill the first 5 bytes of buffer with 'A'
    ft_printf("Buffer content: %s\n", buffer); // Output will be Buffer content: AAAAA

    return 0;
}
```

## Usage

1. **Memory Initialization**: Used to initialize a block of memory with a specific value.
2. **Byte-Level Operation**: Operates on individual bytes within the specified memory region.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
