# d_lst_del_one

## Description

The function **void d_lst_del_one(t_list_d *lst, void (*del)(void *))** deletes a single node (`lst`) from a doubly linked list and frees its memory using the provided `del` function.

The `d_lst_del_one` function deletes the node `lst` from the doubly linked list. It first calls the `del` function to free the memory associated with `lst`'s content (`lst->content`). Then, it frees the memory allocated for `lst` itself and sets `lst` to `NULL`.

## Declaration
```c
void d_lst_del_one(t_list_d *lst, void (*del)(void *));
```
## Parameters

- **lst**: A pointer to the node (`t_list_d`) to be deleted.
- **del**: A pointer to a function that takes a void pointer and deletes the memory associated with the content of the node.

## Return Value

This function does not return a value (void).

## Example

```c
#include "lib_main.h"

// Example delete function for freeing memory of a node's content
void delete_content(void *data) {
    free(data); // Example assumes the content data is dynamically allocated
}

int main() {
    t_list_d *node = create_new_node(); // Assume this function creates a node with dynamically allocated content
    d_lst_del_one(node, delete_content);
    
    // Now 'node' is NULL with its memory freed
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Deleting a Node**: The function deletes the node `lst` from the doubly linked list and frees its content using the provided `del` function.
2. **Memory Deallocation**: It first deallocates the content (`lst->content`) and then deallocates the node `lst` itself.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
