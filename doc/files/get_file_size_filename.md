# get_file_size_filename

## Description

The function **int get_file_size_filename(char *filename)** retrieves the size of a file specified by `filename`. It opens the file using `open` with read-only permissions, retrieves the file size using `get_file_size_fd`, and then closes the file descriptor.

## Declaration

```c
int get_file_size_filename(char *filename);
```

## Parameters

- **filename**: The path to the file whose size is to be retrieved.

## Return Value

Returns the size of the file in bytes as an integer (`int`). Returns `-1` on failure (e.g., if the file cannot be opened or if there are errors retrieving the file size).

## Example

```c
#include "lib_main.h"

// Assume get_file_size_fd is defined in lib_main.h

int main() {
    char *filename = "example.txt";
    
    int file_size = get_file_size_filename(filename);
    if (file_size == -1) {
        perror("Error getting file size");
        return -1;
    }
    
    printf("File size of %s: %d bytes\n", filename, file_size);
    
    return 0;
}
```

## Usage

1. **File Opening**: It opens the file specified by `filename` using `open` with read-only permissions.
2. **Size Retrieval**: It calls `get_file_size_fd` to retrieve the size of the file.
3. **File Closing**: It closes the file descriptor after retrieving the file size.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
