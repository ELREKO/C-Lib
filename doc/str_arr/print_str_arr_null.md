# print_str_arr_null

## Description

The function **void print_str_arr_null(char **arr)** prints each string from a null-terminated string array `arr` to the standard error stream (`stderr`). If `arr` is `NULL`, it prints `"(null)"` to indicate that the array is empty. Each string is printed on a new line using `ft_printf_fd(2, "%s\n", *arr)`.

## Declaration

```c
void print_str_arr_null(char **arr);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) whose elements will be printed to `stderr`.

## Return Value

This function does not return a value (`void`).

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    print_str_arr_null(array);
    return 0;
}
```



## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
