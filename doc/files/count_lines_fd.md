# count_lines_fd

## Description

The function **int count_lines_fd(int fd)** counts the number of lines in a file associated with the given file descriptor (`fd`). It reads the file in chunks using a buffer (`BUFFER_SIZE`) and counts the newline characters (`'\n'`) to determine the total number of lines.

## Declaration

```c
int count_lines_fd(int fd);
```

## Parameters

- **fd**: File descriptor of the file whose lines are to be counted.

## Return Value

Returns the number of lines in the file as an integer (`int`). Returns `0` if the file is empty or if no lines are found. Returns `-1` on failure (e.g., if there are errors reading from the file).

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
    
    int num_lines = count_lines_fd(fd);
    if (num_lines == -1) {
        perror("Error counting lines");
        close(fd);
        return -1;
    }
    
    printf("Number of lines in the file: %d\n", num_lines);
    
    close(fd);
    return 0;
}
```

## Usage

1. **File Reading**: It reads the file descriptor (`fd`) in chunks using a buffer (`BUFFER_SIZE`).
2. **Line Counting**: It counts the newline characters (`'\n'`) in each buffer chunk to determine the total number of lines in the file.
3. **Error Handling**: It returns `-1` if there are errors reading from the file or if no newline characters are found in the file.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
