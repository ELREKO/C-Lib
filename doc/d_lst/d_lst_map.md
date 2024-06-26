# d_lst_map

## Description

The function **t_list_d *d_lst_map(t_list_d *lst, void *(*f)(void *), void (*del)(void *))** applies a function `f` to each element of a doubly linked list `lst`, creating a new list with the results.

The `d_lst_map` function iterates through the doubly linked list `lst`, starting from the head, and applies the function `f` to each node's content (`lst->content`). It creates a new node for each result obtained from `f` and adds it to a new doubly linked list `new_head`. If memory allocation fails during the creation of new nodes, it deletes the newly created list using the function `del` and returns `NULL`.

## Declaration
```c
t_list_d *d_lst_map(t_list_d *lst, void *(*f)(void *), void (*del)(void *));
```
## Parameters

- **lst**: A pointer to the head of the original doubly linked list (`t_list_d`).
- **f**: A pointer to a function that takes a void pointer (the content of a node) and returns a void pointer.
- **del**: A pointer to a function that takes a void pointer (the content of a node) and deletes its memory.

## Return Value

- Returns a pointer to the head of the new doubly linked list (`t_list_d`) containing the results of applying `f` to each node's content in `lst`.
- Returns `NULL` if memory allocation fails or if `lst` is `NULL`.

## Example

```c
#include "lib_main.h"

// Example function to convert content to uppercase
void *convert_to_upper(void *data) {
    char *str = (char *)data;
    char *result = strdup(str); // Example: Allocate memory for the result
    if (result == NULL) {
        return NULL;
    }
    for (int i = 0; result[i] != '\0'; i++) {
        result[i] = toupper(result[i]);
    }
    return result;
}

// Example function to free memory of a string
void delete_string(void *data) {
    free(data); // Example assumes the data is dynamically allocated
}

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume this function creates a populated list
    t_list_d *new_list = d_lst_map(list, convert_to_upper, delete_string);
    
    if (new_list != NULL) {
        printf("New list after mapping:\n");
        d_lst_iter_content(new_list, print_content); // Assume print_content function prints the content
        d_lst_clear(&new_list, delete_string); // Free memory of the new list
    } else {
        printf("Mapping failed or original list is empty.\n");
    }
    
    return 0;
}
```
## Internal Functions

- **d_lst_iter_content**: Used internally to iterate through the content of nodes in a list.
- **d_lst_clear**: Used internally to clear a list and free its memory.

### Usage

1. **Mapping the List**: The function applies the function `f` to each node's content in `lst` and creates a new list (`new_head`) with the results.
2. **Error Handling**: If memory allocation fails during node creation, it deletes the new list using `del` and returns `NULL`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
