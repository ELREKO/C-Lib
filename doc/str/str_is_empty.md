# str_is_empty

## Description

The function **int str_is_empty(const char *str)** determines whether a given string `str` is empty or NULL. It returns 1 if `str` is either NULL or an empty string (`""`), otherwise it returns 0.

## Declaration

```c
int str_is_empty(const char *str);
```

## Parameters

- **str**: Pointer to the string to be checked (`const char *`).

## Return Value

- Returns 1 if `str` is NULL or an empty string (`""`).
- Returns 0 if `str` contains any characters.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "";
    const char *str2 = NULL;
    const char *str3 = "Hello";

    printf("str1 is empty: %d\n", str_is_empty(str1));
    printf("str2 is empty: %d\n", str_is_empty(str2));
    printf("str3 is empty: %d\n", str_is_empty(str3));

    return 0;
}
```

## Usage

1. **Empty String Check**: Determines if `str` is an empty string (`""`) or NULL.
2. **Edge Cases**: Handles NULL pointers safely without causing undefined behavior.
3. **Return Values**: Provides a clear 1 or 0 result based on the emptiness of `str`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
