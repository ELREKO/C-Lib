# ft_calloc

## Description

The function **void *ft_calloc(size_t nmemb, size_t size)** allocates memory for an array of **nmemb** elements of **size** bytes each and initializes the memory to zero.

## Declaration

```c
void *ft_calloc(size_t nmemb, size_t size);
```

## Parameters

- **nmemb**: Number of elements to allocate.
- **size**: Size of each element, in bytes.

## Return Value

- If successful, the function returns a pointer to the allocated memory.
- If allocation fails, it returns **NULL**.

## Example

```c
#include "lib_main.h"

int main() {
    int *arr;
    size_t num_elements = 5;
    
    // Allocate memory for 5 integers
    arr = (int *)ft_calloc(num_elements, sizeof(int));
    
    if (arr) {
        for (size_t i = 0; i < num_elements; ++i) {
            ft_printf("arr[%zu] = %d\n", i, arr[i]); // Output will be arr[0] = 0, arr[1] = 0, ..., arr[4] = 0
        }
        
        free(arr); // Free allocated memory
    } else {
        ft_printf("Memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **Memory Allocation**: The function is used to allocate memory for an array of elements, initializing them to zero.
2. **Checking Allocation**: It checks if memory allocation was successful before using the allocated memory.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
