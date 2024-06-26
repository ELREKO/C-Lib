# d_lst_is_first

## Description

The function **bool d_lst_is_first(t_list_d *lst)** checks if a given node `lst` is the first node in a doubly linked list.

The `d_lst_is_first` function examines the node `lst` to determine if it is the first node in a doubly linked list. It returns `true` if `lst` is the first node (i.e., `lst->prev` is `NULL`). If `lst` is `NULL`, indicating an empty list, the function returns `false`.

## Declaration
```c
bool d_lst_is_first(t_list_d *lst);
```
## Parameters

- **lst**: A pointer to the node (`t_list_d`) to be checked.

## Return Value

- Returns `true` if `lst` is the first node in the list.
- Returns `false` otherwise, including the case where `lst` is `NULL` or it is not the first node.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    bool result = d_lst_is_first(list);
    
    if (result) {
        printf("The node is the first node in the list.\n");
    } else {
        printf("The node is not the first node in the list.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Checking the Node**: The function checks if the node `lst` is the first node in the doubly linked list by examining its `prev` pointer.
2. **Return Value**: It returns `true` if `lst` is the first node, otherwise `false`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
