
# ft_arr_set_int

## Description

The function **size_t ft_arr_set_int(int *arr, size_t size, int num)** sets all elements of an integer array `arr` to a specified integer `num`. It iterates through the array and assigns the value `num` to each element.

## Declaration

```c
size_t ft_arr_set_int(int *arr, size_t size, int num);
```

## Parameters

- **arr**: Pointer to the integer array whose elements are to be set.
- **size**: Size of the integer array `arr`.
- **num**: Integer value to which each element in the array `arr` is set.

## Return Value

Returns the number of elements in the array `arr` (i.e., `size`). If `size` is zero, it returns zero.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    int arr[] = {0, 0, 0, 0, 0};
    size_t size = sizeof(arr) / sizeof(arr[0]);
    int num = 42;

    size_t num_elements_set = ft_arr_set_int(arr, size, num);

    printf("Array after setting all elements to %d:\n", num);
    for (size_t i = 0; i < size; ++i) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    printf("Number of elements set: %zu\n", num_elements_set);

    return 0;
}
```

## Usage

1. **Setting Array Elements**: The function iterates through the integer array `arr` and assigns each element the value `num`.
2. **Return Value**: Returns the number of elements in the array `arr`.
3. **Edge Case**: Handles the case where `size` is zero by returning zero.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
