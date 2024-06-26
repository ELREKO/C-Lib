# ft_lstmap

## Description

The function **t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))** creates a new linked list resulting from applying the function `f` to each element of the original linked list `lst`.

The `ft_lstmap` function iterates through each element of the linked list `lst`. For each element, it applies the function `f` to the content of the element (`lst->content`). It then creates a new element with the transformed content using `ft_lstnew`, and adds this new element to the end of the new linked list. If any allocation fails during this process, it frees the newly created list using `ft_lstclear` with the `del` function and returns `NULL`.

## Declaration

```c
t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
```

## Parameters

- **lst**: A pointer to the first element of the original linked list.
- **f**: The function to apply to each element's content, which returns a pointer to the transformed content.
- **del**: The function to delete the content of an element in case of allocation failure.

## Return Value

- Returns a pointer to the first element of the new linked list created by applying `f` to each element of `lst`.
- Returns `NULL` if allocation fails during the creation of the new linked list.

## Example

```c
#include "lib_main.h"
#include <stdlib.h>
#include <stdio.h>

// Example function to transform content of a list element
void *transform_content(void *content) {
    char *new_content = malloc(strlen(content) + 1);
    if (new_content) {
        strcpy(new_content, content);
        // Example transformation: Convert to uppercase
        for (int i = 0; new_content[i]; i++) {
            new_content[i] = toupper(new_content[i]);
        }
    }
    return new_content;
}

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

    // Map the list to create a new list with transformed content
    t_list *new_list = ft_lstmap(list, transform_content, delete_content);

    // Print the transformed content of the new list
    t_list *temp = new_list;
    while (temp) {
        printf("%s\n", (char *)temp->content);
        temp = temp->next;
    }

    // Clean up: Delete the new list
    ft_lstclear(&new_list, delete_content);

    return 0;
}
```

## Usage

1. **Transformation Function**: The function `f` (such as `transform_content` in the example) transforms the content of each element in the original list `lst`.
2. **Creating New List**: It creates a new list by applying `f` to each element's content and adds the transformed elements to the new list using `ft_lstadd_back`.
3. **Error Handling**: If allocation fails during the creation of the new list, it frees the memory of the new list using `ft_lstclear` with `del` and returns `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
