# d_lst_iter_content

## Description

The function **void d_lst_iter_content(t_list_d *lst, void (*f)(void *))** iterates through a doubly linked list `lst` and applies the function `f` to each element's content.

The `d_lst_iter_content` function iterates through the doubly linked list `lst`, starting from the head, and applies the function `f` to each node's content (`lst->content`). If `lst` is `NULL`, indicating an empty list, the function returns without performing any actions.

## Declaration
```c
void d_lst_iter_content(t_list_d *lst, void (*f)(void *));
```
## Parameters

- **lst**: A pointer to the head of the doubly linked list (`t_list_d`).
- **f**: A pointer to a function that takes a void pointer and applies an operation on the content of each node.

## Return Value

This function does not return a value (void).

## Example

```c
#include "lib_main.h"

// Example function to print content
void print_content(void *data) {
    printf("%s\n", (char *)data); // Example assumes the content is a string
}

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    d_lst_iter_content(list, print_content);
    
    // This would print each element's content in the list
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Iterating through the List**: The function iterates through the doubly linked list `lst`, applying the function `f` to each node's content.
2. **Applying Function `f`**: It calls `f` with the content of each node in the list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
