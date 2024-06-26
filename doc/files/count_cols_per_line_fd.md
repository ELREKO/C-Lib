
# count_cols_per_line_fd

## Description

The function **int count_cols_per_line_fd(int fd, t_file_info *file_info)** counts the number of columns per line in a file descriptor (`fd`) using a specified separator (`file_info->sep`). It reads the file in chunks using a buffer and updates the `file_info->cols` array with the number of columns for each line.

## Declaration

```c
int count_cols_per_line_fd(int fd, t_file_info *file_info);
```

## Parameters

- **fd**: File descriptor of the file to be read.
- **file_info**: Pointer to a `t_file_info` structure containing information about the file and its columns.

## Return Value

Returns `1` on success, `-1` on failure (e.g., if memory allocation fails or if there's an error reading from the file).

## Example

```c
#include "lib_main.h"

// Assume t_file_info and BUFFER_SIZE are defined in lib_main.h

int main() {
    int fd = open("example.txt", O_RDONLY);
    t_file_info file_info;
    file_info.sep = ','; // Example separator
    file_info.rows = 0; // Assume this is initialized properly
    
    int result = count_cols_per_line_fd(fd, &file_info);
    if (result == 1) {
        // Successfully counted columns per line
        for (int i = 0; i < file_info.rows; i++) {
            printf("Line %d has %d columns.\n", i, file_info.cols[i]);
        }
    } else {
        // Handle error
        printf("Error counting columns per line.\n");
    }
    
    close(fd);
    return 0;
}
```

## Usage

1. **File Reading**: It reads the file descriptor (`fd`) in chunks using a buffer (`BUFFER_SIZE`).
2. **Buffer Parsing**: It parses each buffer chunk using `parse_buffer` to count columns per line based on the specified separator (`file_info->sep`).
3. **Line Handling**: It updates the `file_info->cols` array with the number of columns for each line encountered.
4. **Error Handling**: It returns `-1` if there's an error reading from the file or if memory allocation for `file_info->cols` fails.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
