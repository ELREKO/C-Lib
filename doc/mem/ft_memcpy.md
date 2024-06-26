# ft_memcpy

## Description

The function **void *ft_memcpy(void *dest, const void *src, size_t n)** copies **n** bytes from memory area **src** to memory area **dest**. The memory areas must not overlap.

## Declaration

```c
void *ft_memcpy(void *dest, const void *src, size_t n);
```

## Parameters

- **dest**: Pointer to the destination memory area where data is to be copied.
- **src**: Pointer to the source memory area from where data is to be copied.
- **n**: Number of bytes to copy.

## Return Value

- Returns a pointer to **dest**, which is the same as **dest**.

## Example

```c
#include "lib_main.h"

int main() {
    char src[] = "Hello, World!";
    char dest[20];

    ft_memcpy(dest, src, 13); // Copy the first 13 characters from src to dest
    ft_printf("Copied string: %s\n", dest); // Output will be Copied string: Hello, World!

    return 0;
}
```

## Usage

1. **Memory Copy**: Used to copy a specified number of bytes from one memory location to another.
2. **Overlapping Regions**: It's essential that **dest** and **src** do not overlap; for overlapping memory regions, consider using **ft_memmove** instead.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
