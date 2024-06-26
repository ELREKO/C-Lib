# ft_lstclear

## Description

The function **void ft_lstclear(t_list **lst, void (*del)(void *))** deletes and frees the memory of every element in the linked list `lst`, using the function `del` to delete the content of each element.

The `ft_lstclear` function iterates through each element of the linked list starting from `*lst`. For each element, it calls `del` to delete the content of the element, then frees the memory allocated for the element itself. Finally, it sets `*lst` to `NULL` to indicate that the list is now empty.

## Declaration

```c
void ft_lstclear(t_list **lst, void (*del)(void *));
```

## Parameters

- **lst**: A pointer to a pointer to the first element of the linked list.
- **del**: The function used to delete the content of each element.

## Return Value

This function does not return a value.

## Example

```c
#include "lib_main.h"
#include <stdlib.h>

// Example function to delete content of a list element
void delete_content(void *content) {
    free(content); // Example assumes content is dynamically allocated
}

int main() {
    t_list *list = NULL; // Initialize an empty list
    t_list *elem1 = ft_lstnew("first");
    t_list *elem2 = ft_lstnew("second");

    ft_lstadd_back(&list, elem1);
    ft_lstadd_back(&list, elem2);

    // Delete and clear the entire list
    ft_lstclear(&list, delete_content);

    // Now `list` is NULL, and memory for "first" and "second" is freed

    return 0;
}
```

## Internal Functions

### ft_lstdelone

The `ft_lstdelone` function is used internally to delete and free the memory of a single element in the linked list.

### Usage

1. **Initialization**: The function assumes `*lst` points to the beginning of a linked list.
2. **Iterating and Deleting**: It iterates through each element of the list, deletes its content using `del`, and frees the memory of each element using `ft_lstdelone`.
3. **Final Cleanup**: It sets `*lst` to `NULL` after all elements have been deleted to indicate an empty list.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
