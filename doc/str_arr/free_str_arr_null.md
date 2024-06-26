# free_str_arr_null

## Description

The function **void free_str_arr_null(char **str_arr)** frees the memory allocated to an array of strings (`str_arr`). It first iterates through each string in the array and frees the memory allocated to it using `free()`. After freeing each string, it sets the corresponding pointer in the array to `NULL`. Finally, it frees the memory allocated to the array itself (`str_arr`).

## Declaration

```c
void free_str_arr_null(char **str_arr);
```

## Parameters

- **str_arr**: Pointer to an array of strings (`char **`).

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
    free_str_arr_null(str_arr);

    return 0;
}
```

## Usage

1. **Memory Deallocation**: Frees memory allocated to an array of strings.
2. **Safety**: Sets each string pointer in `str_arr` to `NULL` after freeing to prevent accidental use of freed memory (`NULL` is typically a safer state than a dangling pointer).
3. **Cleanup**: Ensures proper cleanup of dynamically allocated memory to prevent memory leaks.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
