# ft_strlcpy

## Description

The function **size_t ft_strlcpy(char *dst, const char *src, size_t size)** copies the string `src` into the buffer `dst`, ensuring null-termination. It copies at most `size - 1` characters from `src` into `dst`, and always null-terminates `dst`. It returns the length of `src`.

## Declaration

```c
size_t ft_strlcpy(char *dst, const char *src, size_t size);
```

## Parameters

- **dst**: Pointer to the destination buffer (`char *`).
- **src**: Pointer to the source string to be copied (`const char *`).
- **size**: Maximum size of the destination buffer (`size_t`).

## Return Value

- Returns the total length of `src` (excluding the null-terminator).
- If `size` is 0 or `dst` is NULL, returns the length of `src` without copying anything.
- Ensures `dst` is null-terminated, even if truncation occurs.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char dst[20];
    char *src = "Hello, World!";
    size_t result_len = ft_strlcpy(dst, src, sizeof(dst));

    printf("Copied string: %s\n", dst);
    printf("Length of source string: %zu\n", result_len);

    return 0;
}
```

## Usage

1. **String Copy**: Safely copies `src` into `dst` ensuring no buffer overflow.
2. **Buffer Size**: Handles the maximum size `size` of the destination buffer.
3. **Return Value**: Provides the length of `src`, even if truncated, ensuring null-termination of `dst`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
