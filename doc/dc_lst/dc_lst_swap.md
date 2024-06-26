
# dc_lst_swap

## Description

The function **t_list_d *dc_lst_swap(t_list_d **lst)** swaps adjacent nodes in a doubly linked list.

The `dc_lst_swap` function takes a double pointer to the head of a doubly linked list (`lst`). It swaps adjacent nodes starting from the head of the list. Depending on the number of nodes (`head` and its adjacent node), it calls either `swap_2` or `swap_3` to perform the swap operations. After swapping, it returns a pointer to the updated list head.

## Declaration

```c
t_list_d *dc_lst_swap(t_list_d **lst);
```

## Parameters

- **lst**: A double pointer to the head node (`t_list_d`) of a doubly linked list.

## Return Value

Returns a pointer to the updated head of the doubly linked list (`t_list_d`). If the list or the head (`*lst`) is `NULL`, it returns `NULL`.

## Example

```c
#include "lib_main.h"

// Assume t_list_d is defined in lib_main.h

int main() {
    t_list_d node1, node2, node3;
    
    // Initialize nodes and links
    node1.next = &node2;
    node2.prev = &node1;
    node2.next = &node3;
    node3.prev = &node2;
    
    t_list_d *head = &node1;
    dc_lst_swap(&head);
    
    // After swap operation, head may point to the new head of the list
    return 0;
}
```

## Usage

1. **Initialization**: It initializes a double pointer to the head of the list (`lst`) and assigns it to `head`.
2. **Node Swapping**: It swaps adjacent nodes in the list using either `swap_2` or `swap_3`, depending on the number of nodes.
3. **Return Value**: It returns a pointer to the updated head of the list after swapping.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)

