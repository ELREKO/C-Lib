# dc_lst_iter_content

## Description

The function **void dc_lst_iter_content(t_list_d *lst, void (*f)(void *))** iterates through a doubly circular linked list `lst` and applies the function `f` to each node's content.

The `dc_lst_iter_content` function iterates through the doubly circular linked list `lst` starting from the head and applies the function `f` to each node's content (`content`). It stops when it reaches the head node again (`head == current`). If `lst` is `NULL`, the function returns without performing any actions.

## Declaration
```c
void dc_lst_iter_content(t_list_d *lst, void (*f)(void *));
```
## Parameters

- **lst**: A pointer to the head of the doubly circular linked list (`t_list_d`).
- **f**: A pointer to the function (`void (*f)(void *)`) to be applied to each node's content.

## Return Value

- Void. Applies the function `f` to each node's content in the doubly circular linked list `lst`.

## Example

```c
#include "lib_main.h"

// Assume function f to print content of each node
void print_content(void *content) {
    printf("Content: %s\n", (char *)content);
}

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    
    dc_lst_iter_content(list, print_content);
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Iterating and Applying Function**: The function iterates through the doubly circular linked list `lst` and applies the function `f` to each node's content.
2. **Content Function**: It uses the provided `f` function to perform an action on each node's content.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
