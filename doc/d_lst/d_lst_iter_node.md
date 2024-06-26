# d_lst_iter_node

## Description

The function **void d_lst_iter_node(t_list_d *lst, void (*f)(void *))** iterates through a doubly linked list `lst` and applies the function `f` to each node.

The `d_lst_iter_node` function iterates through the doubly linked list `lst`, starting from the head, and applies the function `f` to each node (`lst` itself). If `lst` is `NULL`, indicating an empty list, the function returns without performing any actions.

## Declaration
```c
void d_lst_iter_node(t_list_d *lst, void (*f)(void *));
```
## Parameters

- **lst**: A pointer to the head of the doubly linked list (`t_list_d`).
- **f**: A pointer to a function that takes a void pointer and applies an operation on each node of the list.

## Return Value

This function does not return a value (void).

## Example

```c
#include "lib_main.h"

// Example function to print node address
void print_node_address(void *node) {
    printf("Node address: %p\n", node);
}

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    d_lst_iter_node(list, print_node_address);
    
    // This would print the address of each node in the list
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Iterating through the List**: The function iterates through the doubly linked list `lst`, applying the function `f` to each node.
2. **Applying Function `f`**: It calls `f` with each node in the list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
