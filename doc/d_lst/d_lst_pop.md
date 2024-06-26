# d_lst_pop

## Description

The function **t_list_d *d_lst_pop(t_list_d **lst)** removes the first node from a doubly linked list `lst` and returns a pointer to the removed node.

The `d_lst_pop` function removes the node at the head of the doubly linked list `lst`. It adjusts the `prev` pointer of the new head node (if it exists) and sets the `prev` and `next` pointers of the removed node to `NULL`. If `lst` is `NULL` or points to an empty list (`*lst` is `NULL`), the function returns `NULL` without performing any actions.

## Declaration
```c
t_list_d *d_lst_pop(t_list_d **lst);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list (`t_list_d`). This pointer is updated to point to the new head node after the removal.

## Return Value

- Returns a pointer to the removed node (`t_list_d`).
- Returns `NULL` if `lst` is `NULL` or points to an empty list.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *removed_node = d_lst_pop(&list); // Remove the first node
    
    if (removed_node != NULL) {
        printf("First node removed successfully.\n");
        free(removed_node->content); // Example: Free content of the removed node
        free(removed_node); // Free the removed node itself
    } else {
        printf("Failed to remove the first node.\n");
    }
    
    return 0;
}
```
## Internal Functions

- **d_lst_exactly_one**: Used internally to check if the list has exactly one node.

### Usage

1. **Removing the First Node**: The function removes the node at the head of the doubly linked list `lst`.
2. **Return Value**: It returns a pointer to the removed node, allowing further operations on it or freeing its memory.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
