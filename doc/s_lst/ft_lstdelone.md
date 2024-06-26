# ft_lstdelone

## Description

The function **void ft_lstdelone(t_list *lst, void (*del)(void *))** deletes a single element `lst` from a linked list and frees its allocated memory, using the function `del` to delete the content of the element.

The `ft_lstdelone` function first calls `del` to delete the content of the element `lst`. Then, it frees the memory allocated for the element `lst` itself.

## Declaration

```c
void ft_lstdelone(t_list *lst, void (*del)(void *));
```

## Parameters

- **lst**: A pointer to the element of the linked list to be deleted.
- **del**: The function used to delete the content of the element.

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
    t_list *elem = ft_lstnew("element");

    // Delete a single element from the list
    ft_lstdelone(elem, delete_content);

    // Now `elem` is deleted and memory for "element" is freed

    return 0;
}
```

## Usage

1. **Deleting Content**: The function assumes `del` correctly deletes the content of the element pointed to by `lst`.
2. **Freeing Memory**: It then frees the memory allocated for the element `lst` itself.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
