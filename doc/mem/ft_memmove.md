# ft_memmove

## Description

The function **void *ft_memmove(void *dest, const void *src, size_t n)** copies **n** bytes from memory area **src** to memory area **dest**. It handles overlapping memory regions by copying in a safe manner to avoid data corruption.

## Declaration

```c
void *ft_memmove(void *dest, const void *src, size_t n);
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

    ft_memmove(dest, src, 13); // Copy the first 13 characters from src to dest
    ft_printf("Copied string: %s\n", dest); // Output will be Copied string: Hello, World!

    return 0;
}
```

## Internal Functions

### handle_critical_overlap

```c
static void handle_critical_overlap(unsigned char *dest_u, unsigned char *src_u, size_t n);
```

- **Description**: Handles the case where **src** and **dest** memory areas overlap in a critical manner.

### handle_standard_case

```c
static void handle_standard_case(unsigned char *dest_u, unsigned char *src_u, size_t n);
```

- **Description**: Handles the standard case where **src** and **dest** memory areas do not overlap.

## Usage

1. **Memory Move**: Used to move a specified number of bytes from one memory location to another.
2. **Overlapping Regions**: Safely handles overlapping memory regions to prevent data corruption.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
