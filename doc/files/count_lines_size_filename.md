# count_lines_size_filename

## Description

The function **int count_lines_size_filename(char *filename, t_file_info *file_info)** counts the number of lines in a file specified by `filename` and also calculates the total size of the file in bytes (`file_info->file_size`). It opens the file using `open` with read-only permissions, counts the lines and size using `count_lines_size_fd`, and then closes the file descriptor.

## Declaration

```c
int count_lines_size_filename(char *filename, t_file_info *file_info);
```

## Parameters

- **filename**: The path to the file whose lines and size are to be counted.
- **file_info**: Pointer to a `t_file_info` structure where information about the file size (`file_info->file_size`) will be stored.

## Return Value

Returns the number of lines in the file as an integer (`int`). Returns `-1` on failure (e.g., if the file cannot be opened or if there are errors counting lines or size).

## Example

```c
#include "lib_main.h"

// Assume t_file_info and count_lines_size_fd are defined in lib_main.h

int main() {
    char *filename = "example.txt";
    t_file_info file_info;
    
    int num_lines = count_lines_size_filename(filename, &file_info);
    if (num_lines == -1) {
        perror("Error counting lines and size");
        return -1;
    }
    
    printf("Number of lines in the file %s: %d\n", filename, num_lines);
    printf("File size: %ld bytes\n", file_info.file_size);
    
    return 0;
}
```

## Usage

1. **File Opening**: It opens the file specified by `filename` using `open` with read-only permissions.
2. **Line and Size Counting**: It calls `count_lines_size_fd` to count the number of lines in the file and calculate the file size in bytes.
3. **File Closing**: It closes the file descriptor after counting lines and size.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
