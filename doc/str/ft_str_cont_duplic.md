# ft_str_cont_duplic

## Description

The function **int ft_str_cont_duplic(const char *str)** checks if there are any duplicate characters in the string `str`. It returns `1` if there is at least one character that appears more than once in the string, otherwise it returns `0`.

## Declaration

```c
int ft_str_cont_duplic(const char *str);
```

## Parameters

- **str**: The null-terminated string to be checked (`const char *`).

## Return Value

- Returns `1` if there are duplicate characters in the string `str`.
- Returns `0` if all characters in the string `str` are unique.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "hello";
    const char *str2 = "world";
    
    if (ft_str_cont_duplic(str1)) {
        printf("String '%s' contains duplicate characters.\n", str1);
    } else {
        printf("String '%s' does not contain duplicate characters.\n", str1);
    }
    
    if (ft_str_cont_duplic(str2)) {
        printf("String '%s' contains duplicate characters.\n", str2);
    } else {
        printf("String '%s' does not contain duplicate characters.\n", str2);
    }
    
    return 0;
}
```

## Usage

1. **Duplicate Detection**: The function checks each character in `str` and maintains a count of its occurrences.
2. **Return Value**: Returns `1` if any character appears more than once, otherwise `0`.
3. **Character Set**: Supports all ASCII characters (0-255).

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
