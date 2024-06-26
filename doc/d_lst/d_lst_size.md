# d_lst_size

## Description

The function **int d_lst_size(t_list_d *lst)** calculates and returns the number of nodes in a doubly linked list `lst`.

The `d_lst_size` function traverses the doubly linked list `lst`, starting from the head, and counts each node until it reaches the end (`lst->next` is `NULL`). If `lst` is `NULL`, indicating an empty list, the function returns `0`.

## Declaration
```c
int d_lst_size(t_list_d *lst);
```
## Parameters

- **lst**: A pointer to the head of the doubly linked list (`t_list_d`).

## Return Value

- Returns the number of nodes in the doubly linked list `lst`.
- Returns `0` if `lst` is `NULL` (empty list).

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    int size = d_lst_size(list);
    printf("Size of the list: %d\n", size);
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Calculating List Size**: The function traverses the doubly linked list `lst` to count the number of nodes.
2. **Edge Case**: It handles cases where `lst` is `NULL` by returning `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
