# dc_lst_clear

## Description

The function **void dc_lst_clear(t_list_d **lst, void (*del)(void *))** clears a doubly circular linked list `lst`, deallocating memory for each node using the provided deletion function `del`.

The `dc_lst_clear` function traverses the doubly circular linked list `lst` starting from the head (`*lst`) and deallocates memory for each node using the deletion function `del`. It stops when it reaches the head node again (`head == current`). If `lst` is `NULL` or points to an empty list (`*lst` is `NULL`), the function returns without performing any actions.

## Declaration
```c
void dc_lst_clear(t_list_d **lst, void (*del)(void *));
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly circular linked list (`t_list_d`).
- **del**: A pointer to the function that deallocates memory for the content of each node.

## Return Value

- Void. Modifies the list `lst` by deallocating memory for each node and setting `*lst` to `NULL`.

## Example

```c
#include "lib_main.h"

// Assume del function to free content of each node
void del(void *content) {
    free(content);
}

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    
    dc_lst_clear(&list, del);
    
    printf("List cleared successfully.\n");
    
    return 0;
}
```
## Internal Functions

- **dc_lst_del_one**: Used internally to delete a single node from the doubly circular linked list.

### Usage

1. **Clearing the List**: The function deallocates memory for each node in the doubly circular linked list `lst`.
2. **Deletion Function**: It uses the provided `del` function to free the content of each node.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
