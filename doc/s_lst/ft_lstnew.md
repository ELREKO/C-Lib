# ft_lstnew

## Description

The function **t_list *ft_lstnew(void *content)** creates a new linked list element with the given `content`.

The `ft_lstnew` function allocates memory for a new `t_list` structure (`lst_ptr`) and initializes its `content` and `next` pointer. If memory allocation fails, it returns `NULL`. Otherwise, it assigns the `content` parameter to `lst_ptr->content` and sets `lst_ptr->next` to `NULL`, indicating that this element is currently the last in the list.

## Declaration

```c
t_list *ft_lstnew(void *content);
```

## Parameters

- **content**: The content to be added to the new element.

## Return Value

- Returns a pointer to the newly allocated `t_list` structure containing `content`.
- Returns `NULL` if memory allocation fails.

## Example

```c
#include "lib_main.h"
#include <stdlib.h>
#include <stdio.h>

int main() {
    // Create a new list element with content "Hello"
    t_list *new_elem = ft_lstnew("Hello");

    if (new_elem) {
        printf("Content of the new element: %s\n", (char *)new_elem->content); // Output will be "Hello"
    } else {
        printf("Failed to create a new element\n");
    }

    return 0;
}
```

## Usage

1. **Creating New Element**: The function creates a new element for a linked list with the specified content.
2. **Memory Allocation**: It handles memory allocation for the new element and initializes its content and next pointer.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
