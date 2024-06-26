# dc_lst_del_one

## Description

The function **void dc_lst_del_one(t_list_d *lst, void (*del)(void *))** deletes a single node `lst` from a doubly circular linked list and deallocates memory for it using the provided deletion function `del`.

The `dc_lst_del_one` function deallocates memory for the node `lst` and its content using the deletion function `del`. It sets `lst` to `NULL` after deletion. If `lst` is `NULL`, the function returns without performing any actions.

## Declaration
```c
void dc_lst_del_one(t_list_d *lst, void (*del)(void *));
```
## Parameters

- **lst**: A pointer to the node (`t_list_d`) to be deleted from the doubly circular linked list.
- **del**: A pointer to the function that deallocates memory for the content of the node.

## Return Value

- Void. Deletes the node `lst` from the list and deallocates memory for it.

## Example

```c
#include "lib_main.h"

// Assume del function to free content of each node
void del(void *content) {
    free(content);
}

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    t_list_d *node_to_delete = list->next; // Assume node to delete
    
    dc_lst_del_one(node_to_delete, del);
    
    printf("Node deleted successfully.\n");
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Deleting a Node**: The function deletes the node `lst` from the doubly circular linked list and deallocates memory for it.
2. **Deletion Function**: It uses the provided `del` function to free the content of the node.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
