# int_arr_int_index

## Description

The function **int int_arr_int_index(int *arr, int search, int arr_len)** searches for the first occurrence of an integer `search` in the array `arr` with length `arr_len`. If the integer is found, the index of its first occurrence is returned. If the integer is not found, the function returns `-1`.

## Declaration

```c
int int_arr_int_index(int *arr, int search, int arr_len);
```

## Parameters

- **arr**: Pointer to the integer array to be searched.
- **search**: The integer value to search for in the array `arr`.
- **arr_len**: The length of the integer array `arr`.

## Return Value

Returns the index of the first occurrence of `search` in the array `arr`. If `search` is not found in the array, the function returns `-1`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    int arr[] = {4, 2, 7, 5, 9};
    int search = 7;
    int arr_len = sizeof(arr) / sizeof(arr[0]);

    int index = int_arr_int_index(arr, search, arr_len);

    if (index != -1) {
        printf("Element %d found at index %d\n", search, index);
    } else {
        printf("Element %d not found in the array\n", search);
    }

    return 0;
}
```

## Usage

1. **Search Array**: The function iterates through the array `arr` to find the first occurrence of the integer `search`.
2. **Return Index**: If the integer is found, the function returns its index. If the integer is not found, it returns `-1`.
3. **Edge Case**: Handles the case where the array does not contain the `search` integer by returning `-1`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
