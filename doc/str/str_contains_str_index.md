# str_contains_str_index

## Description

The function **int str_contains_str_index(const char *big, const char *little)** searches for the first occurrence of the substring `little` within the string `big`. It returns the index of the first occurrence if found, or -1 if `little` is not found or if either `big` or `little` is NULL.

## Declaration

```c
int str_contains_str_index(const char *big, const char *little);
```

## Parameters

- **big**: Pointer to the string in which to search for `little` (`const char *`).
- **little**: Pointer to the substring to search for within `big` (`const char *`).

## Return Value

- Returns the index (starting from 0) of the first occurrence of `little` within `big`.
- Returns -1 if `little` is not found within `big` or if either `big` or `little` is NULL.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *str1 = "Hello world";
    const char *str2 = "world";
    const char *str3 = "universe";

    int index1 = str_contains_str_index(str1, str2);
    int index2 = str_contains_str_index(str1, str3);

    printf("'%s' contains '%s' at index: %d\n", str1, str2, index1);
    printf("'%s' contains '%s' at index: %d\n", str1, str3, index2);

    return 0;
}
```

## Usage

1. **Substring Search**: Finds the index of the first occurrence of `little` within `big`.
2. **Handling NULL Pointers**: Returns -1 if either `big` or `little` is NULL.
3. **Indexing**: Returns the index of the first character of `little` within `big` if found.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
