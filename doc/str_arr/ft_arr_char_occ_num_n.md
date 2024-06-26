# ft_arr_char_occ_num_n

## Description

The function **int ft_arr_char_occ_num_n(char **arr, char *val)** counts the occurrences of a substring `val` within a string array `arr`. It searches each string in `arr` to find occurrences that match the substring `val` up to the first `=` character. It increments a counter (`num_occ`) for each match found and returns the total count.

## Declaration

```c
int ft_arr_char_occ_num_n(char **arr, char *val);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) where occurrences will be counted.
- **val**: A pointer to a null-terminated string (`char *`) representing the substring to search for, up to the first `=` character.

## Return Value

This function returns an integer (`int`) representing the number of occurrences of `val` within the array `arr`.

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"key1=value1", "key2=value2", "key1=value3"};
    char *substring = "key1";
    int count = ft_arr_char_occ_num_n(array, substring);
    printf("Number of occurrences of '%s' in the array: %d\n", substring, count); // Output will be "Number of occurrences of 'key1' in the array: 2"
    return 0;
}
```

## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
