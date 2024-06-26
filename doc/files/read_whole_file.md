# read_whole_file

## Description

The function **int read_whole_file(int fd, char **res)** reads the entire content of a file associated with the given file descriptor (`fd`) into a dynamically allocated string (`*res`). It reads the file in chunks using a buffer (`BUFFER_SIZE`) and concatenates each chunk to `*res`. Memory allocation for `*res` is handled by `ft_str_n_dup_int` and `ft_str_n_join_int`. If successful, `*res` contains the entire content of the file upon completion.

## Declaration

```c
int read_whole_file(int fd, char **res);
```

## Parameters

- **fd**: File descriptor of the file to be read.
- **res**: Pointer to a pointer to char (`char **`) where the content of the file will be stored.

## Return Value

Returns `0` upon successful completion, indicating that the entire file has been read and stored in `*res`. Returns `-1` on failure (e.g., if there are errors reading from the file or if memory allocation fails).

## Example

```c
#include "lib_main.h"

// Assume BUFFER_SIZE, ft_str_n_dup_int, and ft_str_n_join_int are defined in lib_main.h

int main() {
    int fd = open("example.txt", O_RDONLY);
    if (fd == -1) {
        perror("Error opening file");
        return -1;
    }
    
    char *content = NULL;
    int result = read_whole_file(fd, &content);
    if (result == -1) {
        perror("Error reading file");
        close(fd);
        return -1;
    }
    
    printf("File content:\n%s\n", content);
    
    close(fd);
    free(content); // Remember to free allocated memory
    
    return 0;
}
```

## Usage

1. **File Reading**: It reads the file descriptor (`fd`) in chunks using a buffer (`BUFFER_SIZE`).
2. **Content Concatenation**: It concatenates each chunk of the file to `*res` using `ft_str_n_join_int`.
3. **Memory Management**: It dynamically allocates memory for `*res` using `ft_str_n_dup_int` and `ft_str_n_join_int`, handling reallocation as needed.

---

# free_res_code

## Description

The function **static int free_res_code(char **res, int code)** frees the memory allocated for a dynamically allocated string (`*res`) and returns the provided `code`. It is used internally by `read_whole_file` to free `*res` upon encountering an error condition.

## Declaration

```c
static int free_res_code(char **res, int code);
```

## Parameters

- **res**: Pointer to a pointer to char (`char **`) to be freed.
- **code**: Integer code to be returned after freeing `*res`.

## Return Value

Returns the provided `code` after freeing `*res`.

## Example

This function is typically used internally by other functions like `read_whole_file` to handle memory deallocation upon error conditions.

## Usage

1. **Memory Deallocation**: It frees the memory allocated for `*res`.
2. **Error Handling**: It returns the provided `code`, typically `-1`, after freeing `*res`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
