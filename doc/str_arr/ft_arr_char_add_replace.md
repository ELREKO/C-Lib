# ft_arr_char_add_replace_n

## Description

The function **char **ft_arr_char_add_replace_n(char **arr, char *val)** replaces an element in a string array (`arr`) with a new value (`val`). It first removes the element `val` from the array using `ft_arr_char_rem_n`. If the removal is successful, it then adds the new value `val` to the modified array using `ft_arr_char_add`. Memory allocated for the removed array (`removed`) is freed using `free_str_arr_null`.

## Declaration

```c
char **ft_arr_char_add_replace_n(char **arr, char *val);
```

## Parameters

- **arr**: A pointer to a string array (`char **`) where the replacement operation will be performed.
- **val**: A pointer to a string (`char *`) that will replace an existing element in `arr`.

## Return Value

This function returns a new string array (`char **`) that includes the replaced or added element (`val`). If memory allocation fails or if the removal operation fails, it returns `NULL`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    char *new_value = "orange";
    char **result = ft_arr_char_add_replace_n(array, new_value);
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

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
