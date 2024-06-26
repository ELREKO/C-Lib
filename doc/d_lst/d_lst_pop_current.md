# d_lst_pop_current

## Description

The function **t_list_d *d_lst_pop_current(t_list_d **lst)** removes the current node from a doubly linked list `lst` and returns a pointer to the removed node.

The `d_lst_pop_current` function removes the node currently pointed to by `*lst` from the doubly linked list `lst`. It adjusts the `prev` and `next` pointers of adjacent nodes accordingly. If `lst` is `NULL` or points to an empty list (`*lst` is `NULL`), the function returns `NULL` without performing any actions.

## Declaration
```c
t_list_d *d_lst_pop_current(t_list_d **lst);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list (`t_list_d`). This pointer is updated to point to the next node in the list after the current node is removed.

## Return Value

- Returns a pointer to the removed node (`t_list_d`).
- Returns `NULL` if `lst` is `NULL` or points to an empty list.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *removed_node = d_lst_pop_current(&list);
    
    if (removed_node != NULL) {
        printf("Node removed successfully.\n");
        free(removed_node->content); // Example: Free content of the removed node
        free(removed_node); // Free the removed node itself
    } else {
        printf("Failed to remove a node.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Removing the Current Node**: The function removes the current node pointed to by `*lst` from the doubly linked list and updates `*lst` to point to the next node.
2. **Return Value**: It returns a pointer to the removed node, allowing further operations on it or freeing its memory.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
