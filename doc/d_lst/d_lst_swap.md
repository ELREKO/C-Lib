# d_lst_swap

## Description

The function **t_list_d *d_lst_swap(t_list_d **lst)** swaps adjacent nodes in a doubly linked list `lst` and returns a pointer to the new head of the list.

The `d_lst_swap` function swaps adjacent nodes starting from the head of the doubly linked list `lst`. It utilizes helper functions `swap_2` and `swap_3` based on the number of adjacent nodes to be swapped. If `lst` is `NULL` or points to a list with less than two nodes, the function returns `NULL` without performing any actions.

## Declaration
```c
t_list_d *d_lst_swap(t_list_d **lst);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list (`t_list_d`). This pointer is updated to point to the new head node after swapping.

## Return Value

- Returns a pointer to the new head of the doubly linked list `lst` after swapping adjacent nodes.
- Returns `NULL` if `lst` is `NULL` or points to a list with less than two nodes.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *new_head = d_lst_swap(&list);
    
    if (new_head != NULL) {
        printf("Adjacent nodes swapped successfully.\n");
        // Perform operations on the new list
    } else {
        printf("Failed to swap adjacent nodes.\n");
    }
    
    return 0;
}
```
## Internal Functions

- **swap_2**: Used internally to swap two adjacent nodes in the list.
- **swap_3**: Used internally to swap three adjacent nodes in the list.

### Usage

1. **Swapping Adjacent Nodes**: The function swaps adjacent nodes starting from the head of the doubly linked list `lst`.
2. **Return Value**: It returns a pointer to the new head of the list after swapping, allowing further operations on the list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
