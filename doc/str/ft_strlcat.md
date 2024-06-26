# ft_strlcat

## Description

The function **size_t ft_strlcat(char *dst, const char *src, size_t size)** appends the string `src` to the end of `dst`, while ensuring that the total length does not exceed `size - 1` characters (including the null-terminator). It guarantees null-termination of the result if `size` is greater than the length of `dst`.

## Declaration

```c
size_t ft_strlcat(char *dst, const char *src, size_t size);
```

## Parameters

- **dst**: Pointer to the destination string (`char *`).
- **src**: Pointer to the source string to be appended (`const char *`).
- **size**: Maximum size of the destination buffer including null-terminator (`size_t`).

## Return Value

- Returns the total length of the concatenated string that would have been created if enough space had been available (excluding the null-terminator).
- If the return value exceeds `size - 1`, it indicates truncation, meaning that the entire `src` string did not fit into `dst`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char dst[20] = "Hello";
    char *src = " World!";
    size_t result_len = ft_strlcat(dst, src, sizeof(dst));

    printf("Concatenated string: %s\n", dst);
    printf("Length of concatenated string: %zu\n", result_len);

    return 0;
}
```

## Usage

1. **Concatenation**: Concatenates `src` to `dst` ensuring no buffer overflow.
2. **Buffer Size**: Handles the maximum size `size` of the destination buffer, including the null-terminator.
3. **Return Value**: Provides the total length of the concatenated string that would have been created if enough space had been available.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
