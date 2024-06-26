# dc_lst_size

## Description

The function **int dc_lst_size(t_list_d *lst)** calculates the size (number of nodes) of a doubly linked list.

The `dc_lst_size` function takes a pointer to the head of a doubly linked list (`lst`), where each node is of type `t_list_d`, as defined in `lib_main.h`. It iterates through the list starting from the head and counts each node until it reaches the end of the list, determined when it cycles back to the head node (`head == lst`). The size of the list is returned as an integer value.

## Declaration

int dc_lst_size(t_list_d *lst);

## Parameters

- **lst**: A pointer to the head node (`t_list_d`) of a doubly linked list.

## Return Value

Returns the number of nodes (size) in the doubly linked list as an integer (`int`). If the provided list (`lst`) is `NULL`, it returns `0`.

## Example

```c
#include "lib_main.h"

// Assume t_list_d is defined in lib_main.h

int main() {
    t_list_d node1, node2, node3;
    
    // Initialize nodes and links
    node1.next = &node2;
    node2.next = &node3;
    node3.next = &node1; // circular list
    
    int size = dc_lst_size(&node1);
    printf("Size of the list: %d\n", size); // Output: Size of the list: 3
    
    return 0;
}
```
---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)