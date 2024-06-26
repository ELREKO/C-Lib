# dc_lst_print_one_str_long

## Description

The function **void dc_lst_print_one_str_long(void *lst_ptr_void)** prints detailed information about a node in a doubly linked list containing strings.

The `dc_lst_print_one_str_long` function takes a pointer to a node (`lst_ptr_void`) of type `t_list_d`, which is a structure defined in `lib_main.h`. It prints information about the node's pointers (`prev`, `own`, `next`) and their corresponding contents using helper functions (`print_format_ptr` and `print_format_cont`). Each pointer is printed alongside its label (`prev ptr:`, `own ptr:`, `next ptr:`), and each content is printed alongside its label (`prev cont:`, `own cont:`, `next cont:`). After printing, it calls `dc_lst_print_sep` to print a separator, assuming this function is defined elsewhere in the program.

## Declaration
```c
void dc_lst_print_one_str_long(void *lst_ptr_void);
```
## Parameters

- **lst_ptr_void**: A pointer to a node (`t_list_d`) of a doubly linked list.

## Return Value

This function does not return a value (`void`).

## Example
```c
#include "lib_main.h"

// Assume t_list_d is defined in lib_main.h

int main() {
    t_list_d node1, node2, node3;
    char *data1 = "First";
    char *data2 = "Second";
    char *data3 = "Third";
    
    node1.content = data1;
    node2.content = data2;
    node3.content = data3;
    
    node1.prev = NULL;
    node1.next = &node2;
    node2.prev = &node1;
    node2.next = &node3;
    node3.prev = &node2;
    node3.next = NULL;
    
    dc_lst_print_one_str_long(&node2);
    return 0;
}
```
## Usage

1. **Node Validation**: It checks if the provided node pointer (`lst_ptr_void`) is not NULL.
2. **Printing Pointers and Contents**: It uses `print_format_ptr` to print pointer information and `print_format_cont` to print content information for the previous, current, and next nodes in the list.
3. **Separator Printing**: It calls `dc_lst_print_sep` after printing the node information.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
