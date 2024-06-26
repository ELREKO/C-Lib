# d_lst_add_front

## Description

The function **void d_lst_add_front(t_list_d **lst, t_list_d *new)** adds the element pointed to by `new` to the front of a doubly linked list `lst`.

The `d_lst_add_front` function adds the element `new` to the front of a doubly linked list pointed to by `lst`. If `new` is `NULL`, the function returns without making any changes. If the list is empty (`*lst` is `NULL`), `new` becomes the first and only element in the list. Otherwise, `new` is inserted at the front of the list, and pointers are updated accordingly.

## Declaration
```c
void d_lst_add_front(t_list_d **lst, t_list_d *new);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list.
- **new**: A pointer to the new element (`t_list_d`) to be added to the front of the list.

## Return Value

This function does not return a value (void).

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = NULL;
    t_list_d *node1 = create_new_node();
    t_list_d *node2 = create_new_node();
    
    d_lst_add_front(&list, node1);
    d_lst_add_front(&list, node2);
    
    // Now list points to a doubly linked list with node2 followed by node1
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Adding a New Node**: If `new` is not `NULL`, the function checks if the list is empty (`*lst` is `NULL`). If so, `new` becomes the first element. Otherwise, `new` is inserted at the front, and pointers are updated to maintain the doubly linked structure.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
