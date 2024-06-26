
# count_cols_per_line_filename

## Description

The function **int count_cols_per_line_filename(char *filename, t_file_info *file_info)** counts the number of columns per line in a file specified by `filename` using a file descriptor. It utilizes the `count_lines_fd` and `count_cols_per_line_fd` functions to determine the number of lines and columns respectively, populating the `file_info` structure with this information.

## Declaration

```c
int count_cols_per_line_filename(char *filename, t_file_info *file_info);
```

## Parameters

- **filename**: The path to the file whose columns per line are to be counted.
- **file_info**: Pointer to a `t_file_info` structure where information about the file and its columns will be stored.

## Return Value

Returns `1` on success, `-1` on failure (e.g., if the file cannot be opened or if there are errors in counting lines or columns).

## Example

```c
#include "lib_main.h"

// Assume t_file_info, count_lines_fd, and count_cols_per_line_fd are defined in lib_main.h

int main() {
    char *filename = "example.csv";
    t_file_info file_info;
    
    int result = count_cols_per_line_filename(filename, &file_info);
    if (result == 1) {
        // Successfully counted columns per line
        for (int i = 0; i < file_info.rows; i++) {
            printf("Line %d has %d columns.\n", i, file_info.cols[i]);
        }
    } else {
        // Handle error
        printf("Error counting columns per line in file %s.\n", filename);
    }
    
    return 0;
}
```

## Usage

1. **File Opening**: It opens the file specified by `filename` using `open` with read-only permissions.
2. **Line Counting**: It calls `count_lines_fd` to determine the number of lines in the file and stores this in `file_info->rows`.
3. **Column Counting**: It opens the file again and calls `count_cols_per_line_fd` to count the number of columns per line, storing this information in `file_info->cols`.
4. **Error Handling**: It returns `-1` if there are errors opening or reading the file, or if either line or column counting functions fail.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
