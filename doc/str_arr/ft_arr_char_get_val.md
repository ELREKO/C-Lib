# ft_arr_char_get_val

## Description

The function **char *ft_arr_char_get_val(char **arr, char *key)** retrieves the value associated with a specific key from a string array `arr`. It searches through each string in `arr` to find an entry that starts with `key`, followed by an `=` character. If such an entry is found, it returns a duplicate (`ft_strdup`) of the substring that follows the `=` character. If no matching entry is found, it returns `NULL`.

## Declaration

```c
char *ft_arr_char_get_val(char **arr, char *key);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) where the key-value pair will be searched.
- **key**: A pointer to a null-terminated string (`char *`) representing the key to search for.

## Return Value

This function returns a newly allocated string (`char *`) containing the value associated with `key`, or `NULL` if the key is not found or if memory allocation fails.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"key1=value1", "key2=value2", "key3=value3"};
    char *key_to_find = "key2";
    char *value = ft_arr_char_get_val(array, key_to_find);
    if (value) {
        printf("Value for key '%s' is '%s'\n", key_to_find, value); // Output will be "Value for key 'key2' is 'value2'"
        free(value); // Free memory allocated for value
    } else {
        printf("Key '%s' not found\n", key_to_find);
    }
    return 0;
}
```

## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
