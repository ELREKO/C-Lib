# print_int_arr

## Description

The function **void print_int_arr(int *arr, int num)** prints the elements of an integer array `arr` to the standard output, with each element printed on a new line. The number of elements to print is specified by `num`.

## Declaration
```c
void print_int_arr(int *arr, int num);
```
## Parameters

- **arr**: Pointer to the integer array to be printed.
- **num**: The number of elements in the array `arr` to be printed.

## Return Value

This function does not return a value.

## Example
```c
#include "lib_main.h"

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int num = sizeof(arr) / sizeof(arr[0]);

    print_int_arr(arr, num);

    return 0;
}
```
## Usage

1. **Print Elements**: The function iterates through the first `num` elements of the array `arr`, printing each element followed by a newline character.
2. **Iteration**: Uses a simple loop to iterate over the elements of the array.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
