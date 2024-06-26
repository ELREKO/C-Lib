# count_lines_size_fd

## Description

The function **int count_lines_size_fd(int fd, t_file_info *file_info)** counts the number of lines in a file associated with the given file descriptor (`fd`) and also calculates the total size of the file in bytes (`file_info->file_size`). It reads the file in chunks using a buffer (`BUFFER_SIZE`) and counts the newline characters (`'\n'`) to determine the total number of lines.

## Declaration

```c
int count_lines_size_fd(int fd, t_file_info *file_info);
```

## Parameters

- **fd**: File descriptor of the file whose lines and size are to be counted.
- **file_info**: Pointer to a `t_file_info` structure where information about the file size (`file_info->file_size`) will be stored.

## Return Value

Returns the number of lines in the file as an integer (`int`). Returns `0` if the file is empty or if no lines are found. Returns `-1` on failure (e.g., if there are errors reading from the file).

## Example

```c
#include "lib_main.h"

// Assume t_file_info and BUFFER_SIZE are defined in lib_main.h

int main() {
    int fd = open("example.txt", O_RDONLY);
    if (fd == -1) {
        perror("Error opening file");
        return -1;
    }
    t_file_info file_info;
    
    int num_lines = count_lines_size_fd(fd, &file_info);
    if (num_lines == -1) {
        perror("Error counting lines and size");
        close(fd);
        return -1;
    }
    
    printf("Number of lines in the file: %d\n", num_lines);
    printf("File size: %ld bytes\n", file_info.file_size);
    
    close(fd);
    return 0;
}
```

## Usage

1. **File Reading**: It reads the file descriptor (`fd`) in chunks using a buffer (`BUFFER_SIZE`).
2. **Line and Size Counting**: It counts the newline characters (`'\n'`) in each buffer chunk to determine the total number of lines in the file. It also accumulates the total size of the file in bytes (`file_info->file_size`).
3. **Error Handling**: It returns `-1` if there are errors reading from the file or if no newline characters are found in the file.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
