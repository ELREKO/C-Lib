# ft_lstadd_front

## Description

The function **void ft_lstadd_front(t_list **lst, t_list *new)** adds the element `new` at the beginning of the linked list `lst`.

The `ft_lstadd_front` function inserts the element `new` at the front of the linked list pointed to by `lst`. It updates the `next` pointer of `new` to point to the current head of the list (`*lst`), and then updates `*lst` to point to `new`, making `new` the new head of the list.

## Declaration

```c
void ft_lstadd_front(t_list **lst, t_list *new);
```

## Parameters

- **lst**: A pointer to a pointer to the first element of the linked list.
- **new**: The element to add at the beginning of the linked list.

## Return Value

This function does not return a value.

## Example

```c
#include "lib_main.h"

int main() {
    t_list *list = NULL; // Initialize an empty list
    t_list *elem1 = ft_lstnew("first");
    t_list *elem2 = ft_lstnew("second");

    ft_lstadd_front(&list, elem2); // Add "second" to the front
    ft_lstadd_front(&list, elem1); // Add "first" to the front

    // Now `list` contains "first" followed by "second"
    
    return 0;
}
```

## Usage

1. **Initialization**: The function assumes `*lst` points to `NULL` initially, indicating an empty list.
2. **Adding New Element**: It updates the `next` pointer of `new` to point to the current head of the list (`*lst`), and then updates `*lst` to point to `new`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
