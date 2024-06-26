# dc_lst_exactly_two

## Description

The function **int dc_lst_exactly_two(t_list_d *lst_ptr)** checks if a doubly circular linked list `lst_ptr` contains exactly two nodes.

The `dc_lst_exactly_two` function checks if the doubly circular linked list `lst_ptr` contains exactly two nodes. It returns `1` if `lst_ptr` is not `NULL` and points to a list where `lst_ptr->next->next` points back to `lst_ptr`, indicating exactly two nodes in the list. Otherwise, it returns `0`.

## Declaration
```c
int dc_lst_exactly_two(t_list_d *lst_ptr);
```
## Parameters

- **lst_ptr**: A pointer to the head of the doubly circular linked list (`t_list_d`).

## Return Value

- Returns `1` if the doubly circular linked list `lst_ptr` contains exactly two nodes.
- Returns `0` otherwise, including when `lst_ptr` is `NULL` or does not contain exactly two nodes.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list_with_two_nodes(); // Assume this function creates a list with exactly two nodes
    
    int result = dc_lst_exactly_two(list);
    
    if (result == 1) {
        printf("The list contains exactly two nodes.\n");
    } else {
        printf("The list does not contain exactly two nodes.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Checking Number of Nodes**: The function checks if the doubly circular linked list `lst_ptr` contains exactly two nodes.
2. **Return Value**: It returns `1` if the list has exactly two nodes, otherwise `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
