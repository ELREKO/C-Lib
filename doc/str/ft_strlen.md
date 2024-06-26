# ft_strlen

## Description

The function **size_t ft_strlen(const char *s)** calculates the length of the null-terminated string `s`. It counts and returns the number of characters in `s` up to, but not including, the null terminator ('\0').

## Declaration

```c
size_t ft_strlen(const char *s);
```

## Parameters

- **s**: Pointer to the null-terminated string whose length is to be calculated (`const char *`).

## Return Value

- Returns the number of characters in `s` excluding the null terminator ('\0').

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *str = "Hello, World!";
    size_t length = ft_strlen(str);

    printf("Length of the string '%s' is: %zu\n", str, length);

    return 0;
}
```

## Usage

1. **String Length**: Computes the length of the string `s`.
2. **Null Terminator**: Counts characters until encountering the null terminator ('\0').
3. **Return Value**: Provides the length of the string excluding the null terminator.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
