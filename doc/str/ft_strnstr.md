# ft_strnstr

## Description

The function **char *ft_strnstr(const char *big, const char *little, size_t len)** locates the first occurrence of the null-terminated string `little` in the null-terminated string `big`, where not more than `len` characters are searched. If `little` is an empty string, `big` is returned. If `little` occurs nowhere in `big` or if the length of `little` exceeds `len`, `NULL` is returned.

## Declaration

```c
char *ft_strnstr(const char *big, const char *little, size_t len);
```

## Parameters

- **big**: Pointer to the null-terminated string to search within (`const char *`).
- **little**: Pointer to the null-terminated string to search for (`const char *`).
- **len**: Maximum number of characters to search in `big` (`size_t`).

## Return Value

- Returns a pointer to the first occurrence of `little` within `big`, starting from `big`, or `NULL` if `little` is not found within the first `len` characters of `big`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *big_str = "Hello, world! This is a test string.";
    const char *little_str = "world";
    char *result = ft_strnstr(big_str, little_str, 20);

    if (result)
        printf("Substring found at position: %ld\n", result - big_str);
    else
        printf("Substring not found.\n");

    return 0;
}
```

## Usage

1. **Substring Search**: Searches for the first occurrence of `little` in `big`.
2. **Limited Search**: Searches at most `len` characters in `big`.
3. **Return Value**: Returns a pointer to the start of the found substring within `big` or `NULL` if not found.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
