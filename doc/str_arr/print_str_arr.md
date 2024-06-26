# print_str_arr

## Description

The function **void print_str_arr(char **arr, int num)** prints the first `num` strings from a string array `arr` to the standard output. It iterates through the array and prints each string followed by a newline character using `ft_printf("%s\n", arr[i])`.

## Declaration

```c
void print_str_arr(char **arr, int num);
```

## Parameters

- **arr**: A pointer to a null-terminated string array (`char **`) from which strings will be printed.
- **num**: An integer (`int`) specifying the number of strings to print from `arr`.

## Return Value

This function does not return a value (`void`).

## Example

```c
#include "./lib_main.h"

int main() {
    char *array[] = {"apple", "banana", "cherry"};
    print_str_arr(array, 2); // Print the first 2 strings
    return 0;
}
```

## Internal Functions

### None

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
