# ft_memchr

## Description

The function **void *ft_memchr(const void *s, int c, size_t n)** searches for the first occurrence of the character **c** (interpreted as an unsigned char) in the initial **n** bytes of the object pointed to by **s**.

## Declaration

```c
void *ft_memchr(const void *s, int c, size_t n);
```

## Parameters

- **s**: Pointer to the memory area to be searched.
- **c**: Value to be searched for, typecasted as an `unsigned char`.
- **n**: Number of bytes to be searched.

## Return Value

- If the character **c** is found, a pointer to the first occurrence is returned.
- If **c** is not found within the first **n** bytes, **NULL** is returned.

## Example

```c
#include "lib_main.h"

int main() {
    const char *str = "Hello, World!";
    char *ptr;
    size_t n = ft_strlen(str);
    
    // Search for the character 'W' in the string
    ptr = ft_memchr(str, 'W', n);
    
    if (ptr != NULL) {
        ft_printf("Found 'W' at position %ld\n", ptr - str); // Output will be Found 'W' at position 7
    } else {
        ft_printf("Character not found.\n");
    }
    
    return 0;
}
```

## Usage

1. **Search in Memory**: The function is used to locate a specific character within a memory block.
2. **Returns**: It returns a pointer to the first occurrence of the character if found, or **NULL** if not found within the specified number of bytes.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
