# free_file_info_ptr

## Description

The function **void free_file_info_ptr(t_file_info *file_info)** frees the memory allocated for a `t_file_info` structure and its contents. It first calls `free_file_info` to release memory allocated for the `file_info.cols` array, and then frees the `file_info` structure itself.

## Declaration

```c
void free_file_info_ptr(t_file_info *file_info);
```

## Parameters

- **file_info**: Pointer to a `t_file_info` structure whose memory is to be freed.

## Return Value

None.

## Example

```c
#include "lib_main.h"

// Assume t_file_info and free_file_info are defined in lib_main.h

int main() {
    t_file_info *file_info = malloc(sizeof(t_file_info));
    if (file_info == NULL) {
        perror("Error allocating memory");
        return -1;
    }
    
    // Perform operations with file_info
    
    free_file_info_ptr(file_info);
    
    return 0;
}
```

## Usage

1. **Memory Deallocation**: It frees the memory allocated for the `file_info.cols` array using `free_file_info`.
2. **Structure Deallocation**: It frees the memory allocated for the `file_info` structure itself using `free`.

---

# free_file_info

## Description

The function **void free_file_info(t_file_info file_info)** frees the memory allocated for the `file_info.cols` array.

## Declaration

```c
void free_file_info(t_file_info file_info);
```

## Parameters

- **file_info**: A `t_file_info` structure whose `file_info.cols` array memory is to be freed.

## Return Value

None.

## Example

```c
#include "lib_main.h"

// Assume t_file_info is defined in lib_main.h

int main() {
    t_file_info file_info;
    file_info.cols = malloc(sizeof(int) * 10); // Allocate memory
    
    // Perform operations with file_info
    
    free_file_info(file_info); // Free memory
    
    return 0;
}
```

## Usage

1. **Memory Deallocation**: It frees the memory allocated for the `file_info.cols` array using `free`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
