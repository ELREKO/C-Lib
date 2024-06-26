# ft_str_n_join

## Description

The function **char *ft_str_n_join(const char *s1, const char *s2, int n)** joins up to `n` characters from `s2` onto the end of `s1` and returns a newly allocated string containing the result. If `n` is `0`, it concatenates the entire string `s2`. If either `s1` or `s2` is `NULL`, it duplicates the non-NULL string directly.

## Declaration

```c
char *ft_str_n_join(const char *s1, const char *s2, int n);
```

## Parameters

- **s1**: The null-terminated string to which `s2` will be joined (`const char *`).
- **s2**: The null-terminated string to be joined onto `s1` (`const char *`).
- **n**: The maximum number of characters from `s2` to concatenate onto `s1` (`int`).

## Return Value

- Returns a pointer to a newly allocated string containing the joined result.
- Returns `NULL` if memory allocation fails or if both `s1` and `s2` are `NULL`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *s1 = "Hello, ";
    const char *s2 = "world!";
    char *joined_string = NULL;
    
    joined_string = ft_str_n_join(s1, s2, 0);
    
    if (joined_string) {
        printf("Joined string: %s\n", joined_string);
        free(joined_string);
    } else {
        printf("Joining failed or memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **String Concatenation**: Concatenates up to `n` characters from `s2` onto `s1`.
2. **Memory Allocation**: Allocates memory for the resulting joined string.
3. **Handling `n` Values**: If `n` is `0`, concatenates the entire string `s2` onto `s1`.
4. **Null Checks**: If either `s1` or `s2` is `NULL`, duplicates the non-NULL string directly.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
