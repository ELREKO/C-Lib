# d_lst_last

## Description

The function **t_list_d *d_lst_last(t_list_d *lst)** finds and returns the last node in a doubly linked list `lst`.

The `d_lst_last` function traverses the doubly linked list `lst`, starting from the head, to find the last node. If `lst` is `NULL`, indicating an empty list, the function returns `NULL`. Otherwise, it iterates through the list until it reaches the last node (`last->next` is `NULL`) and returns a pointer to this last node.

## Declaration
```c
t_list_d *d_lst_last(t_list_d *lst);
```
## Parameters

- **lst**: A pointer to the head of the doubly linked list (`t_list_d`).

## Return Value

- Returns a pointer to the last node (`t_list_d`) in the list `lst`.
- Returns `NULL` if `lst` is `NULL` or if the list is empty.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *last_node = d_lst_last(list);
    
    if (last_node != NULL) {
        printf("The address of the last node: %p\n", last_node);
    } else {
        printf("The list is empty.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Finding the Last Node**: The function traverses the doubly linked list `lst` to find and return a pointer to the last node.
2. **Edge Cases**: It handles cases where `lst` is `NULL` or the list is empty by returning `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
