# ft_arr_char_rem_n

## Description

The function **char **ft_arr_char_rem_n(char **arr, char *val)** removes all occurrences of a substring `val` from a string array `arr` and returns a new array (`cpy`) without those occurrences. It initializes necessary values using `init_vals` and iterates through `arr` to copy non-matching strings to `cpy`. Memory allocation for `cpy` is handled internally, and if allocation fails during the process, it frees allocated memory and returns `NULL`.

## Declaration

```c
char **ft_arr_char_rem_n(char **arr, char *val);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) from which occurrences of `val` will be removed.
- **val**: A pointer to a null-terminated string (`char *`) representing the substring to remove from `arr`.

## Return Value

This function returns a new string array (`char **`) that excludes all occurrences of `val` from `arr`. If memory allocation fails or if any operation encounters an error, it returns `NULL`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"key1=value1", "key2=value2", "key1=value3"};
    char *substring = "key1";
    char **result = ft_arr_char_rem_n(array, substring);
    if (result) {
        for (int i = 0; result[i] != NULL; i++) {
            printf("%s\n", result[i]); // Output will be "key2=value2"
        }
        free_str_arr_null(result); // Free memory allocated for result
    }
    return 0;
}
```

## Internal Functions

### init_vals

```c
static int init_vals(t_arr_char_key_info *arr_info, int *i, int *j, char **org_arr);
```

The `init_vals` function initializes necessary values (`key_len`, `arr_len`, `key_occ_n`, `i`, `j`) and allocates memory for the copy array (`cpy`). It returns `1` on failure and `0` on success.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
