# ft_arr_len_char

## Description

The function **size_t ft_arr_len_char(char **arr)** calculates the number of elements in a null-terminated string array `arr`. It iterates through the array until it encounters a `NULL` pointer, counting each non-NULL element as it progresses. If `arr` is `NULL` or if its first element is `NULL`, it returns zero.

## Declaration

```c
size_t ft_arr_len_char(char **arr);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) whose length will be calculated.

## Return Value

This function returns a `size_t` value representing the number of elements in the array `arr`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    size_t length = ft_arr_len_char(array);
    printf("Length of array: %zu\n", length); // Output will be "Length of array: 3"
    return 0;
}
```

## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
