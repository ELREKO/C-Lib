# str_only_spaces

## Description

The function **bool str_only_spaces(char *str)** checks if a given string `str` consists entirely of whitespace characters. It returns `true` if `str` is not NULL and contains only spaces, tabs, newline characters, carriage returns, form feeds, or vertical tabs. If `str` contains any non-whitespace characters or is NULL, it returns `false`.

## Declaration

```c
bool str_only_spaces(char *str);
```

## Parameters

- **str**: Pointer to the string to be checked (`char *`).

## Return Value

- Returns `true` if `str` contains only whitespace characters or is an empty string.
- Returns `false` if `str` contains any non-whitespace characters or is NULL.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *str1 = "    \t\n";   // Only spaces, tabs, and newline
    char *str2 = "Hello";      // Contains non-whitespace characters

    printf("str1 consists only of spaces: %s\n", str_only_spaces(str1) ? "true" : "false");
    printf("str2 consists only of spaces: %s\n", str_only_spaces(str2) ? "true" : "false");

    return 0;
}
```

## Usage

1. **Whitespace Check**: Determines if `str` consists exclusively of whitespace characters.
2. **Edge Cases**: Handles NULL pointers safely without causing undefined behavior.
3. **Return Values**: Provides a clear boolean result (`true` or `false`) based on the contents of `str`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
