# ft_lstiter

## Description

The function **void ft_lstiter(t_list *lst, void (*f)(void *))** applies the function `f` to each element of the linked list `lst`.

The `ft_lstiter` function iterates through each element of the linked list starting from `lst`. For each element, it calls the function `f` and passes the content of the element (`lst->content`) as an argument. This allows `f` to operate on or modify each element's content in the linked list.

## Declaration

```c
void ft_lstiter(t_list *lst, void (*f)(void *));
```

## Parameters

- **lst**: A pointer to the first element of the linked list.
- **f**: The function to apply to each element's content.

## Return Value

This function does not return a value.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

// Example function to print content of a list element
void print_content(void *content) {
    printf("%s\n", (char *)content); // Example assumes content is a string
}

int main() {
    t_list *list = NULL; // Initialize an empty list
    t_list *elem1 = ft_lstnew("first");
    t_list *elem2 = ft_lstnew("second");

    ft_lstadd_back(&list, elem1);
    ft_lstadd_back(&list, elem2);

    // Apply a function to print each element's content
    ft_lstiter(list, print_content);

    // Output will be:
    // first
    // second

    return 0;
}
```

## Usage

1. **Function Application**: The function `f` (such as `print_content` in the example) is applied to each element's content in the linked list `lst`.
2. **Iteration**: It iterates through each element of the list until `lst` is `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
