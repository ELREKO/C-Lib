# remove_spaces_inplace

## Description

The function **int remove_spaces_inplace(char **str)** removes all spaces (' ', '\t', '\n', '\v', '\f', '\r') from the string `*str` in place. It modifies `*str` directly. Returns 0 on successful removal or if `*str` is NULL.

## Declaration

```c
int remove_spaces_inplace(char **str);
```

## Parameters

- **str**: Pointer to a pointer to the string (`char **`) that will have spaces removed.

## Return Value

- Returns 0 on success.
- Returns 1 if `*str` is NULL.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char *str = ft_strdup("Hello,  World!");
    
    printf("Before removing spaces: \"%s\"\n", str);
    remove_spaces_inplace(&str);
    printf("After removing spaces: \"%s\"\n", str);
    
    free(str);
    return 0;
}
```

## Usage

1. **In-Place Modification**: Modifies `*str` directly by shifting characters to overwrite spaces.
2. **Space Removal**: Iterates through the string and shifts characters left when encountering spaces.
3. **Error Handling**: Returns 1 if `*str` is NULL, indicating no operation performed.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
