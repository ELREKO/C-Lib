# ft_arr_char_add

## Description

The function **char **ft_arr_char_add(char **arr, char *val)** adds a new string `val` to an existing string array `arr`. It creates a copy of `arr`, adds `val` to the end of the copy, and returns the modified array. Memory allocation for the copy (`cpy`) is handled internally, and if any allocation fails during the process, it frees allocated memory using `free_null` and returns `NULL`.

## Declaration

```c
char **ft_arr_char_add(char **arr, char *val);
```

## Parameters

- **arr**: A pointer to a string array (`char **`) where the new string `val` will be added.
- **val**: A pointer to a string (`char *`) that will be added to the end of `arr`.

## Return Value

This function returns a new string array (`char **`) that includes the original elements of `arr` plus the added string `val`. If memory allocation fails at any point, it returns `NULL`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    char *new_value = "orange";
    char **result = ft_arr_char_add(array, new_value);
    if (result) {
        for (int i = 0; result[i] != NULL; i++) {
            printf("%s\n", result[i]);
        }
        free_str_arr_null(result); // Free memory allocated for result
    }
    return 0;
}
```

## Internal Functions

### free_null

```c
static char **free_null(char **cpy);
```

The `free_null` function frees the memory allocated for a string array (`cpy`) and returns `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
