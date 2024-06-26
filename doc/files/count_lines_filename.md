
# count_lines_filename

## Description

The function **int count_lines_filename(char *filename)** counts the number of lines in a file specified by `filename`. It opens the file using `open` with read-only permissions, counts the lines using `count_lines_fd`, and then closes the file descriptor.

## Declaration

```c
int count_lines_filename(char *filename);
```

## Parameters

- **filename**: The path to the file whose lines are to be counted.

## Return Value

Returns the number of lines in the file as an integer (`int`). Returns `-1` on failure (e.g., if the file cannot be opened or if there are errors counting lines).

## Example

```c
#include "lib_main.h"

// Assume count_lines_fd is defined in lib_main.h

int main() {
    char *filename = "example.txt";
    
    int num_lines = count_lines_filename(filename);
    if (num_lines == -1) {
        perror("Error counting lines");
        return -1;
    }
    
    printf("Number of lines in the file %s: %d\n", filename, num_lines);
    
    return 0;
}
```

## Usage

1. **File Opening**: It opens the file specified by `filename` using `open` with read-only permissions.
2. **Line Counting**: It calls `count_lines_fd` to count the number of lines in the file.
3. **File Closing**: It closes the file descriptor after counting lines.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
