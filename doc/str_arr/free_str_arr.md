# free_str_arr

## Description

The function **void free_str_arr(char **str_arr, int num)** frees the memory allocated to an array of strings (`str_arr`). It iterates through the array of strings starting from the last element and frees the memory allocated to each string using `free()`. After freeing all strings, it frees the memory allocated to the array (`str_arr`) itself using `free()`.

## Declaration

```c
void free_str_arr(char **str_arr, int num);
```

## Parameters

- **str_arr**: Pointer to an array of strings (`char **`).
- **num**: Number of elements in the array (`int`).

## Return Value

- The function returns `void`.

## Example

```c
#include "lib_main.h"
#include <stdlib.h>

int main() {
    char **str_arr = malloc(3 * sizeof(char *));
    if (!str_arr) {
        // Handle allocation failure
        return 1;
    }

    str_arr[0] = strdup("Hello");
    str_arr[1] = strdup("World");
    str_arr[2] = NULL;

    // Freeing the array of strings
    free_str_arr(str_arr, 3);

    return 0;
}
```

## Usage

1. **Memory Deallocation**: Frees memory allocated to an array of strings and the array itself.
2. **Reverse Order**: Frees strings in reverse order to avoid memory leaks and potential segmentation faults.
3. **Efficient Cleanup**: Cleans up dynamically allocated memory to prevent memory leaks and ensure proper resource management.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
