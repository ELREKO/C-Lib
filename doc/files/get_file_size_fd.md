# get_file_size_fd

## Description

The function **int get_file_size_fd(int fd)** retrieves the size of a file associated with the given file descriptor (`fd`). It reads the file in chunks using a buffer (`BUFFER_SIZE`) and accumulates the total number of bytes read to determine the file size.

## Declaration

```c
int get_file_size_fd(int fd);
```

## Parameters

- **fd**: File descriptor of the file whose size is to be retrieved.

## Return Value

Returns the size of the file in bytes as an integer (`int`). Returns `0` if the file is empty. Returns `-1` on failure (e.g., if there are errors reading from the file).

## Example

```c
#include "lib_main.h"

// Assume BUFFER_SIZE is defined in lib_main.h

int main() {
    int fd = open("example.txt", O_RDONLY);
    if (fd == -1) {
        perror("Error opening file");
        return -1;
    }
    
    int file_size = get_file_size_fd(fd);
    if (file_size == -1) {
        perror("Error getting file size");
        close(fd);
        return -1;
    }
    
    printf("File size: %d bytes\n", file_size);
    
    close(fd);
    return 0;
}
```

## Usage

1. **File Reading**: It reads the file descriptor (`fd`) in chunks using a buffer (`BUFFER_SIZE`).
2. **Size Calculation**: It accumulates the number of bytes read from the file to determine the total file size.
3. **Error Handling**: It returns `-1` if there are errors reading from the file or if the file size cannot be determined.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
