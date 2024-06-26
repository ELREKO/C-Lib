# ft_memcmp

## Description

The function **int ft_memcmp(const void *s1, const void *s2, size_t n)** compares the first **n** bytes of memory areas **s1** and **s2**.

## Declaration

```c
int ft_memcmp(const void *s1, const void *s2, size_t n);
```

## Parameters

- **s1**: Pointer to the first memory area.
- **s2**: Pointer to the second memory area.
- **n**: Number of bytes to compare.

## Return Value

- Returns an integer less than, equal to, or greater than zero if the first **n** bytes of **s1** are found, respectively, to be less than, to match, or be greater than the first **n** bytes of **s2**.

## Example

```c
#include "lib_main.h"

int main() {
    const char str1[] = "Hello";
    const char str2[] = "Hello";
    const char str3[] = "World";
    
    int result1 = ft_memcmp(str1, str2, 5); // Compare the first 5 bytes of str1 and str2
    int result2 = ft_memcmp(str1, str3, 5); // Compare the first 5 bytes of str1 and str3
    
    ft_printf("Comparison result 1: %d\n", result1); // Output will be Comparison result 1: 0
    ft_printf("Comparison result 2: %d\n", result2); // Output will be Comparison result 2: -15
    
    return 0;
}
```

## Usage

1. **Memory Comparison**: The function is used to compare blocks of memory byte by byte.
2. **Returns**: It returns zero if the first **n** bytes of both memory areas are identical. If they differ, it returns a value less than zero if the first differing byte in **s1** is less than that in **s2**, or a value greater than zero otherwise.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
