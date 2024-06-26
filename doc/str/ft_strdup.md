# ft_strdup

## Description

The function **char *ft_strdup(const char *s)** duplicates the string `s`. It allocates sufficient memory for a copy of the string `s`, copies the string into the allocated memory, and returns a pointer to it.

## Declaration

```c
char *ft_strdup(const char *s);
```

## Parameters

- **s**: The string to be duplicated (`const char *`).

## Return Value

- Returns a pointer to the duplicated string if the memory allocation succeeds.
- Returns `NULL` if the memory allocation fails.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    const char *original = "Hello, world!";
    
    char *duplicate = ft_strdup(original);
    
    if (duplicate) {
        printf("Original: %s\n", original);
        printf("Duplicate: %s\n", duplicate);
        free(duplicate); // Remember to free the allocated memory
    } else {
        printf("Memory allocation failed.\n");
    }
    
    return 0;
}
```

## Usage

1. **Memory Allocation**: Allocates memory for a copy of the string `s` using `malloc`.
2. **String Copying**: Copies the characters of `s` into the allocated memory.
3. **Return Values**: Returns a pointer to the duplicated string if successful; otherwise, returns `NULL` if memory allocation fails.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
