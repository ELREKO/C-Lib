# d_lst_add_back

## Description

The function **void d_lst_add_back(t_list_d **lst, t_list_d *new)** adds the element pointed to by `new` to the end of a doubly linked list `lst`.

The `d_lst_add_back` function adds the element `new` to the back of a doubly linked list pointed to by `lst`. If `new` is `NULL`, the function returns without making any changes. If the list is empty (`*lst` is `NULL`), `new` becomes the first and only element in the list. Otherwise, `new` is linked at the end of the list after the last element.

## Declaration
```c
void d_lst_add_back(t_list_d **lst, t_list_d *new);
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list.
- **new**: A pointer to the new element (`t_list_d`) to be added to the list.

## Return Value

This function does not return a value (void).

## Example
```c
#include "lib_main.h"

int main() {
    t_list_d *list = NULL;
    t_list_d *node1 = create_new_node();
    t_list_d *node2 = create_new_node();
    
    d_lst_add_back(&list, node1);
    d_lst_add_back(&list, node2);
    
    // Now list points to a doubly linked list with node1 followed by node2
    return 0;
}
```
## Internal Functions

### d_lst_last

The `d_lst_last` function (not shown here) is used internally to find the last element in the doubly linked list `lst`.

### Usage

1. **Adding a New Node**: If `new` is not `NULL`, the function finds the last element in the list (`last`). If the list is empty (`last` is `NULL`), `new` becomes the first element.
2. **Updating Pointers**: The function updates the `prev` and `next` pointers of `new` and the last element to maintain the doubly linked structure.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
