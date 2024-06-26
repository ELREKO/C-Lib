# d_lst_pop_n

## Description

The function **t_list_d *d_lst_pop_n(t_list_d **lst, int n)** removes the node at position `n` from a doubly linked list `lst` and returns a pointer to the removed node.

The `d_lst_pop_n` function removes the node at the specified position `n` from the doubly linked list `lst`. It adjusts the `prev` and `next` pointers of adjacent nodes accordingly. If `lst` is `NULL` or points to an empty list (`*lst` is `NULL`), or if the position `n` is out of bounds, the function returns `NULL` without performing any actions.

## Declaration
```c
t_list_d *d_lst_pop_n(t_list_d **lst, int n);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list (`t_list_d`). This pointer is updated to point to the next node after the removal.
- **n**: The index (starting from 0) of the node to be removed from the list. Use `-1` to remove the last node.

## Return Value

- Returns a pointer to the removed node (`t_list_d`).
- Returns `NULL` if `lst` is `NULL` or points to an empty list, or if the position `n` is out of bounds.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *removed_node = d_lst_pop_n(&list, 2); // Remove node at index 2
    
    if (removed_node != NULL) {
        printf("Node at index 2 removed successfully.\n");
        free(removed_node->content); // Example: Free content of the removed node
        free(removed_node); // Free the removed node itself
    } else {
        printf("Failed to remove node at index 2.\n");
    }
    
    return 0;
}
```
## Internal Functions

- **d_lst_size**: Used internally to determine the size of the doubly linked list.
- **d_lst_pop**: Used internally to remove the first node from the list.

### Usage

1. **Removing a Node by Index**: The function removes the node at position `n` from the doubly linked list `lst`.
2. **Boundary Checks**: It checks if `lst` is `NULL`, if the list is empty, or if the position `n` is out of bounds before performing any actions.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
