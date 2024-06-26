# ft_arr_cpy_char

## Description

The function **char **ft_arr_cpy_char(char **arr, int num)** creates a deep copy of the first `num` elements of a string array `arr`. It allocates memory for a new array (`cpy`) and duplicates each string from `arr` up to `num` using `ft_strdup`. If any allocation fails during the copying process, it frees the memory allocated so far and returns `NULL`. The copied array `cpy` is terminated with a `NULL` pointer.

## Declaration

```c
char **ft_arr_cpy_char(char **arr, int num);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) from which the first `num` elements will be copied.
- **num**: An integer (`int`) specifying the number of elements to copy from `arr`.

## Return Value

This function returns a newly allocated string array (`char **`) containing duplicates of the first `num` elements from `arr`. If memory allocation fails or if any operation encounters an error, it returns `NULL`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry", "date"};
    int num_elements = 3;
    char **copy = ft_arr_cpy_char(array, num_elements);
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
