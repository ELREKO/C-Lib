# ![book](doc/pic/lib_pic.png) C - Library 📚
These are the first projects of the programming school [42 Berlin](https://42berlin.de/en/). The originally required library, libft, was expanded with additional useful functions during subsequent projects where the custom C library was allowed to be used. The library can be used as an alternative to the standard library. 

## Overview of the Functions [Overview](/doc/Overview_about_function.md)
If there are any issues in the documentation or functionality, I would appreciate a notification.

## Projects
### 1. Library Creation ([libft](doc/PDF/libft_subject.pdf)):
Create your own library with basic functions from the standard C library, such as string manipulation, memory management, and basic mathematical operations.

### 2. Implementation of Printf Functionality ([ft_printf](doc/PDF/ft_printf_subject.pdf)):
Develop your own version of the printf function from the standard C library. This includes understanding and implementing string formatting, variable arguments, and precision control.

### 3. File Processing and Input Management ([get_next_line](doc/PDF/get_next_line_subject.pdf)):
Implement a function to read lines from files or other input streams. This requires mastery of file operations, buffer management, and basic data structures.


## Using the Library

### Using in Your Own Project
1. Navigate to the libft directory.
2. Execute the Makefile with the command:
    ```shell
    make
    ```
3. Include the library in your own projects:
    ```c
    #include "libft/libft.h"
    ```

### Cleaning Object Files (for upload, etc.)
```shell
make clean
make fclean
```





