# ft_arr_cpy_char_null

## Description

The function **char **ft_arr_cpy_char_null(char **arr)** creates a deep copy of a null-terminated string array `arr`. It allocates memory for a new array (`cpy`) and duplicates each string from `arr` using `ft_strdup`. If any allocation fails during the copying process, it frees the memory allocated so far and returns `NULL`. The copied array `cpy` is terminated with a `NULL` pointer.

## Declaration

```c
char **ft_arr_cpy_char_null(char **arr);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) that will be copied.

## Return Value

This function returns a newly allocated string array (`char **`) containing duplicates of the strings from `arr`. If memory allocation fails or if any operation encounters an error, it returns `NULL`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    char **copy = ft_arr_cpy_char_null(array);
    if (copy) {
        for (int i = 0; copy[i] != NULL; i++) {
            printf("%s\n", copy[i]); // Output will be "apple", "banana", "cherry"
        }
        free_str_arr_null(copy); // Free memory allocated for copy
    }
    return 0;
}
```

## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
