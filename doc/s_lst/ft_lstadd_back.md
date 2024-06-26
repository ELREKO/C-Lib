# ft_lstadd_back

## Description

The function **void ft_lstadd_back(t_list **lst, t_list *new)** adds the element `new` at the end of the linked list `lst`.

The `ft_lstadd_back` function appends the given element `new` to the end of the linked list pointed to by `lst`. If the list is initially empty (`*lst` is `NULL`), it sets `*lst` to `new`. Otherwise, it traverses the list to find the last element (`ft_lstlast(*lst)`), and then appends `new` to the `next` pointer of this last element.

## Declaration

```c
void ft_lstadd_back(t_list **lst, t_list *new);
```

## Parameters

- **lst**: A pointer to a pointer to the first element of the linked list.
- **new**: The element to add at the end of the linked list.

## Return Value

This function does not return a value.

## Example

```c
#include "lib_main.h"

int main() {
    t_list *list = NULL; // Initialize an empty list
    t_list *elem1 = ft_lstnew("first");
    t_list *elem2 = ft_lstnew("second");

    ft_lstadd_back(&list, elem1);
    ft_lstadd_back(&list, elem2);

    // Now `list` contains "first" followed by "second"
    
    return 0;
}
```

## Internal Functions

### ft_lstlast

The `ft_lstlast` function is used internally to find the last element of the linked list `lst`.

### Usage

1. **Initialization**: Checks if the list is empty (`*lst == NULL`).
2. **Appending New Element**: If the list is not empty, it finds the last element using `ft_lstlast` and links the new element `new` at the end.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
