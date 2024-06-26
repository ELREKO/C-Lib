# ft_str_chr_index

## Description

The function **ssize_t ft_str_chr_index(const char *s, int c)** searches for the first occurrence of the character `c` in the string `s`. If found, it returns the index of `c` in `s`. If `c` is not found, it returns `-1`.

## Declaration

```c
ssize_t ft_str_chr_index(const char *s, int c);
```

## Parameters

- **s**: Pointer to the null-terminated string to be searched (`const char *`).
- **c**: Character to search for (`int`).

## Return Value

- Returns the index of the first occurrence of `c` in `s`.
- Returns `-1` if `c` is not found in `s`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "Hello, world!";
    int index = ft_str_chr_index(str, 'w');
    if (index != -1) {
        printf("Index of 'w' in '%s' is: %d\n", str, index);
    } else {
        printf("Character 'w' not found in '%s'\n", str);
    }
    return 0;
}
```

## Usage

1. **Searching Character**: The function searches for the character `c` within the string `s`.
2. **Indexing**: Returns the index (zero-based position) of the first occurrence of `c` in `s`.
3. **Error Handling**: Returns `-1` if `c` is not found in `s`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
