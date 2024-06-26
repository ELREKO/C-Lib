# malloc_error_free

## Description

The function **int malloc_error_free(char **res, size_t i_num_substr, size_t substr_len)** attempts to allocate memory for a substring in a dynamic array `res`. If the memory allocation fails for the substring `res[i_num_substr]`, it frees previously allocated memory and returns `0`.

The `malloc_error_free` function first attempts to allocate memory for `res[i_num_substr]` using `malloc`. If successful, it returns `1`. If allocation fails, it iterates through previously allocated substrings and frees each one using `free`. Finally, it frees the entire dynamic array `res` and returns `0` to indicate failure.

## Declaration

```c
int malloc_error_free(char **res, size_t i_num_substr, size_t substr_len);
```

## Parameters

- **res**: Pointer to a dynamic array of strings (`char **`).
- **i_num_substr**: Index of the substring where memory allocation failed.
- **substr_len**: Length of the substring to allocate.

## Return Value

- Returns `1` if memory allocation for `res[i_num_substr]` is successful.
- Returns `0` if memory allocation fails, and frees previously allocated memory.

## Example

```c
#include "lib_main.h"
#include <stdlib.h>

int main() {
    char **res = NULL;
    size_t num_substrings = 5;
    size_t substr_len = 10;

    res = malloc(num_substrings * sizeof(char *));
    if (!res) {
        return -1; // Handle allocation failure
    }

    size_t i;
    for (i = 0; i < num_substrings; i++) {
        if (!malloc_error_free(res, i, substr_len)) {
            printf("Memory allocation failed for substring at index %zu\n", i);
            break;
        }
        // Example: Assign content to res[i]
        strcpy(res[i], "example");
    }

    // Clean up: Free all allocated memory
    if (res) {
        for (i = 0; i < num_substrings; i++) {
            if (res[i]) {
                free(res[i]);
            }
        }
        free(res);
    }

    return 0;
}
```

## Usage

1. **Memory Allocation**: The function attempts to allocate memory for a substring in a dynamic array `res`.
2. **Error Handling**: It handles memory allocation failures by freeing previously allocated memory.
3. **Dynamic Array**: `res` should be a dynamically allocated array of strings (`char **`).

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
