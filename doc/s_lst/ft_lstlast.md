# ft_lstlast

## Description

The function **t_list *ft_lstlast(t_list *lst)** returns the last element of the linked list `lst`.

The `ft_lstlast` function traverses the linked list starting from `lst` to find the last element. If `lst` is `NULL`, indicating an empty list, it returns `NULL`. Otherwise, it iterates through the list until it reaches the last element (`last->next` is `NULL`) and returns a pointer to this last element.

## Declaration

```c
t_list *ft_lstlast(t_list *lst);
```

## Parameters

- **lst**: A pointer to the first element of the linked list.

## Return Value

This function returns a pointer to the last element of the linked list `lst`. If `lst` is `NULL`, it returns `NULL`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    t_list *list = NULL; // Initialize an empty list
    t_list *elem1 = ft_lstnew("first");
    t_list *elem2 = ft_lstnew("second");

    ft_lstadd_back(&list, elem1);
    ft_lstadd_back(&list, elem2);

    t_list *last_elem = ft_lstlast(list);
    if (last_elem)
        printf("Last element: %s\n", (char *)last_elem->content); // Output will be "second"

    return 0;
}
```

## Usage

1. **Finding the Last Element**: The function is used to retrieve a pointer to the last element of the linked list `lst`.
2. **Handling Edge Cases**: It handles cases where `lst` is `NULL` by returning `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
