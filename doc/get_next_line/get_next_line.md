# get_next_line

## Description

The function **char *get_next_line(int fd)** reads a line from a file descriptor (`fd`) and returns it as a dynamically allocated string (`char *`). It implements a mechanism to read line by line until a newline character (`'\n'`) or the end of file (EOF) is encountered.

## Declaration

```c
char *get_next_line(int fd);
```

## Parameters

- **fd**: The file descriptor from which to read the input.

## Return Value

Returns a pointer to the next line read from the file descriptor (`fd`) as a `char *`. If an error occurs or if the end of file is reached, it returns `NULL`.

## Internal Functions

### check_if_newline_in_buffer

```c
int check_if_newline_in_buffer(t_get_next *gnl_info, char **next_line);
```

Checks if there is a newline character (`'\n'`) in the buffer read from the file descriptor.

### process_newline_search_result

```c
int process_newline_search_result(t_get_next *gnl_info, char **next_line, t_search_state search);
```

Processes the search result from `check_if_newline_in_buffer` to handle cases where a newline character is found or not found in the buffer.

### reset_gnl_static_null

```c
char *reset_gnl_static_null(t_get_next *gnl_info, char **next_line);
```

Resets the internal state of `gnl_info` and frees allocated memory when an error occurs during processing.

### reset_gnl_static

```c
void reset_gnl_static(t_get_next *gnl_info);
```

Resets the internal state of `gnl_info` without freeing allocated memory.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    int fd = open("example.txt", O_RDONLY);
    if (fd == -1) {
        perror("Error opening file");
        return -1;
    }

    char *line;
    while ((line = get_next_line(fd)) != NULL) {
        printf("%s\n", line);
        free(line);
    }

    close(fd);
    return 0;
}
```

## Usage

1. **Reading Lines**: The function reads lines from the specified file descriptor (`fd`) until a newline character or EOF is encountered.
2. **Memory Management**: It dynamically allocates memory for each line read, which should be freed by the caller after use.
3. **Error Handling**: Returns `NULL` on error or when the end of file is reached, allowing the caller to handle errors appropriately.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
