# dc_lst_add_front

## Description

The function **void dc_lst_add_front(t_list_d **lst, t_list_d *new)** adds a new node `new` at the front of a doubly circular linked list `lst`.

The `dc_lst_add_front` function adds the node `new` at the front of the doubly circular linked list `lst`. It utilizes the `dc_lst_add_back` function to add `new` at the end of the list and then updates `*lst` to point to `new`, effectively making `new` the new head of the list.

## Declaration
```c
void dc_lst_add_front(t_list_d **lst, t_list_d *new);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly circular linked list (`t_list_d`).
- **new**: A pointer to the node (`t_list_d`) to be added to the front of the list.

## Return Value

- Void. Modifies the list `lst` by adding the node `new` at the front.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    t_list_d *new_node = create_doubly_linked_list_node(); // Assume this function creates a new node
    
    dc_lst_add_front(&list, new_node);
    
    printf("Node added to the front of the list.\n");
    
    return 0;
}
```
## Internal Functions

- **dc_lst_add_back**: Used internally to add a node to the end of the doubly circular linked list.

### Usage

1. **Adding a Node to the Front**: The function adds a new node `new` at the front of the doubly circular linked list `lst`.
2. **Updating the Head**: It updates `*lst` to point to `new`, making `new` the new head of the list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
