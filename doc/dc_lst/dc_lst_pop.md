# dc_lst_pop

## Description

The function **t_list_d *dc_lst_pop(t_list_d **lst)** removes the head node from a doubly circular linked list `lst` and returns a pointer to the removed node.

The `dc_lst_pop` function removes the head node from the doubly circular linked list `lst`. If `lst` is `NULL` or empty (`*lst` is `NULL`), it returns `NULL`. It adjusts the pointers of the neighboring nodes to maintain the circular structure. It returns a pointer to the removed node (`t_list_d`). If the list contains exactly one node after removal, it sets `*lst` to `NULL`.

## Declaration
```c
t_list_d *dc_lst_pop(t_list_d **lst);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly circular linked list (`t_list_d`). The function modifies `*lst` to reflect the new head after removal.

## Return Value

- Returns a pointer to the removed head node (`t_list_d`).
- Returns `NULL` if `lst` is `NULL` or empty (`*lst` is `NULL`).

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    
    t_list_d *removed_node = dc_lst_pop(&list);
    
    if (removed_node == NULL) {
        printf("Failed to pop from empty list.\n");
        return 1;
    }
    
    // Use removed_node
    
    return 0;
}
````
## Internal Functions

None

### Usage

1. **Node Removal**: The function removes the head node from the doubly circular linked list `lst` and returns a pointer to the removed node.
2. **List Adjustment**: It adjusts the pointers of neighboring nodes to maintain the circular structure after removal.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
