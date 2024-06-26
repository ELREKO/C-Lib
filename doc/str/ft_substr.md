# ft_substr

## Description

The function **char *ft_substr(char const *s, unsigned int start, size_t len)** creates a substring from the string `s`. The substring begins at index `start` and has a maximum length of `len` characters (or until the end of `s`, whichever comes first). Returns a newly allocated substring, or `NULL` if memory allocation fails or if `s` is NULL.

## Declaration

```c
char *ft_substr(char const *s, unsigned int start, size_t len);
```

## Parameters

- **s**: Pointer to the null-terminated string from which to create the substring (`const char *`).
- **start**: Starting index of the substring within `s` (`unsigned int`).
- **len**: Maximum length of the substring to extract (`size_t`).

## Return Value

- Returns a newly allocated substring starting from index `start` of `s`, with a maximum length of `len` characters, or until the end of `s`.
- Returns `NULL` if memory allocation fails or if `s` is NULL.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str = "Hello, world!";
    char *sub = ft_substr(str, 7, 5); // "world"

    if (sub) {
        printf("Original string: \"%s\"\n", str);
        printf("Substring: \"%s\"\n", sub);
        free(sub);
    } else {
        printf("Memory allocation failed or input string is NULL.\n");
    }

    return 0;
}
```

## Usage

1. **Substring Extraction**: Extracts a substring from `s` starting at index `start` up to `len` characters long.
2. **Memory Allocation**: Handles memory allocation internally; returns `NULL` on failure.
3. **Edge Cases**: Handles cases where `start` is beyond the end of `s`, `len` is 0, or `s` is NULL by returning an empty string.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
