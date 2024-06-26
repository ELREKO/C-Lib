# dc_lst_add_back

## Description

The function **void dc_lst_add_back(t_list_d **lst, t_list_d *new)** adds a new node `new` at the end of a doubly circular linked list `lst`.

The `dc_lst_add_back` function adds the node `new` at the end of the doubly circular linked list `lst`. If `lst` is `NULL`, the function simply returns without performing any actions. If `new` is `NULL`, it also returns without modifying the list.

## Declaration
```c
void dc_lst_add_back(t_list_d **lst, t_list_d *new);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly circular linked list (`t_list_d`).
- **new**: A pointer to the node (`t_list_d`) to be added to the end of the list.

## Return Value

- Void. Modifies the list `lst` by adding the node `new` at the end.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    t_list_d *new_node = create_doubly_linked_list_node(); // Assume this function creates a new node
    
    dc_lst_add_back(&list, new_node);
    
    printf("Node added to the end of the list.\n");
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Adding a Node to the End**: The function adds a new node `new` at the end of the doubly circular linked list `lst`.
2. **Edge Cases**: It handles cases where `lst` or `new` is `NULL` by returning without modifying the list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
