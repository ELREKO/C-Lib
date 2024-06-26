# ft_lstsize

## Description

The function **int ft_lstsize(t_list *lst)** calculates the number of elements in the linked list `lst` and returns the count.

The `ft_lstsize` function iterates through each element of the linked list starting from `lst`. It increments a counter for each element until it reaches the end of the list (`lst->next` is `NULL`). If `lst` is `NULL`, indicating an empty list, it returns `0`.

## Declaration

```c
int ft_lstsize(t_list *lst);
```

## Parameters

- **lst**: A pointer to the first element of the linked list.

## Return Value

This function returns an integer representing the number of elements in the linked list `lst`.

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

    int size = ft_lstsize(list);
    printf("Size of the list: %d\n", size); // Output will be "2"

    return 0;
}
```

## Usage

1. **Counting Elements**: The function counts the number of elements in the linked list `lst`.
2. **Handling Edge Cases**: It handles cases where `lst` is `NULL` by returning `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
