# ft_strmapi

## Description

The function **char *ft_strmapi(char const *s, char (*f)(unsigned int, char))** applies the function `f` to each character of the null-terminated string `s`, creating a new string resulting from these applications. It allocates memory for the new string, modifies each character based on the index and original character in `s`, and terminates the new string with a null character ('\0').

## Declaration

```c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char));
```

## Parameters

- **s**: Pointer to the null-terminated string to be mapped (`const char *`).
- **f**: Pointer to a function that takes an unsigned integer index and a character as arguments and returns a character (`char (*)(unsigned int, char)`).

## Return Value

- Returns a pointer to a newly allocated string that results from applying the function `f` to each character of `s`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

// Function to convert lowercase letters to uppercase
char toupper_map(unsigned int index, char c) {
    if (c >= 'a' && c <= 'z') {
        return c - 'a' + 'A'; // Convert to uppercase
    }
    return c; // Return unchanged for non-lowercase letters
}

int main() {
    char *str = "hello, world!";
    char *mapped_str = ft_strmapi(str, toupper_map);

    printf("Original string: %s\n", str);
    printf("Mapped string: %s\n", mapped_str);

    free(mapped_str); // Remember to free allocated memory

    return 0;
}
```

## Usage

1. **String Mapping**: Applies the function `f` to each character of the string `s`.
2. **Character Transformation**: Modifies characters based on the function `f` and their respective indices.
3. **Return Value**: Returns a new string reflecting the modifications made by `f`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
