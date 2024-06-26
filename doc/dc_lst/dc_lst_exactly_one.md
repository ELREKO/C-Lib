# dc_lst_exactly_one

## Description

The function **int dc_lst_exactly_one(t_list_d *lst_ptr)** checks if a doubly circular linked list `lst_ptr` contains exactly one node.

The `dc_lst_exactly_one` function checks if the doubly circular linked list `lst_ptr` contains exactly one node. It returns `1` if `lst_ptr` is not `NULL` and points to a single node where `lst_ptr->next` points back to `lst_ptr` itself. Otherwise, it returns `0`.

## Declaration
```c
int dc_lst_exactly_one(t_list_d *lst_ptr);
```
## Parameters

- **lst_ptr**: A pointer to the head of the doubly circular linked list (`t_list_d`).

## Return Value

- Returns `1` if the doubly circular linked list `lst_ptr` contains exactly one node.
- Returns `0` otherwise, including when `lst_ptr` is `NULL`.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list_with_single_node(); // Assume this function creates a list with exactly one node
    
    int result = dc_lst_exactly_one(list);
    
    if (result == 1) {
        printf("The list contains exactly one node.\n");
    } else {
        printf("The list does not contain exactly one node.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Checking Number of Nodes**: The function checks if the doubly circular linked list `lst_ptr` contains exactly one node.
2. **Return Value**: It returns `1` if the list has exactly one node, otherwise `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
