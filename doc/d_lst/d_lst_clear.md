# d_lst_clear

## Description

The function **void d_lst_clear(t_list_d **lst, void (*del)(void *))** clears a doubly linked list `lst`, calling the function `del` on each element to free its memory.

The `d_lst_clear` function iterates through the doubly linked list `lst` starting from the head. It deletes each element by calling the function `del` provided as a parameter. After clearing all elements, the head pointer `*lst` is set to `NULL`.

## Declaration
```c
void d_lst_clear(t_list_d **lst, void (*del)(void *));
```
## Parameters

- **lst**: A pointer to a pointer to the head of the doubly linked list.
- **del**: A pointer to a function that takes a void pointer and deletes the memory associated with the element.

## Return Value

This function does not return a value (void).

## Example

```c
#include "lib_main.h"

// Example delete function for freeing memory of a node
void delete_node(void *data) {
    free(data); // Example assumes the data is dynamically allocated
}

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    d_lst_clear(&list, delete_node);
    
    // Now list points to NULL with all memory freed
    return 0;
}
```
## Internal Functions

### d_lst_del_one

The `d_lst_del_one` function (not shown here) is used internally to delete a single node from the doubly linked list.

### Usage

1. **Clearing the List**: The function iterates through the list, deleting each node and freeing its memory using the provided `del` function.
2. **Setting Head to NULL**: After clearing all nodes, the function sets the head pointer `*lst` to `NULL` to indicate an empty list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
