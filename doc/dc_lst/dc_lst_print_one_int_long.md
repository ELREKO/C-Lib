
# dc_lst_print_one_int_long

## Description

The function **void dc_lst_print_one_int_long(void *lst_ptr_void)** prints information about a node in a doubly circular linked list containing integer content.

The `dc_lst_print_one_int_long` function expects a pointer to a node (`lst_ptr_void`) in a doubly circular linked list (`t_list_d`). It prints:
- The pointer to the previous node (`prev ptr`).
- The content of the previous node (`prev cont`).
- The pointer to the current node (`own ptr`).
- The content of the current node (`own cont`).
- The pointer to the next node (`next ptr`).
- The content of the next node (`next cont`).

It uses helper functions `print_format_cont` and `print_format_ptr` to print formatted information about pointers and content.

## Declaration

```c
void dc_lst_print_one_int_long(void *lst_ptr_void);
```

## Parameters

- **lst_ptr_void**: A pointer to a node (`t_list_d`) in a doubly circular linked list (`void *`). It should point to a valid node in the list.

## Return Value

- The function returns `void`.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    
    // Print information about the first node
    dc_lst_print_one_int_long(list);
    
    return 0;
}
```

### Usage

1. **Node Information Printing**: The function prints detailed information about a node in a doubly circular linked list containing integer content.
2. **Format Helpers**: It utilizes `print_format_cont` and `print_format_ptr` to format and print information about pointers and content.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
