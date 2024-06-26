# dc_lst_map

## Description

The function **t_list_d *dc_lst_map(t_list_d *lst, void *(*f)(void *), void (*del)(void *))** creates a new doubly circular linked list by applying function `f` to each node's content of the input list `lst`.

The `dc_lst_map` function iterates through the doubly circular linked list `lst`, applies the function `f` to each node's content (`content`), and creates a new node with the transformed content in a new doubly circular linked list. It returns a pointer to the head of the new list. If `lst` is `NULL` or memory allocation fails, it returns `NULL`.

## Declaration
```c
t_list_d *dc_lst_map(t_list_d *lst, void *(*f)(void *), void (*del)(void *));
```
## Parameters

- **lst**: A pointer to the head of the original doubly circular linked list (`t_list_d`).
- **f**: A pointer to the function (`void *(*f)(void *)`) to be applied to each node's content. It transforms the content.
- **del**: A pointer to the function (`void (*del)(void *)`) used to free the content of nodes if memory allocation fails.

## Return Value

- Returns a pointer to the head of the new doubly circular linked list containing transformed content.
- Returns `NULL` if `lst` is `NULL` or memory allocation fails during the creation of the new list.

## Example

```c
#include "lib_main.h"

// Assume function f to transform content of each node
void *transform_content(void *content) {
    // Example: Transforming string content to uppercase
    char *str = (char *)content;
    char *transformed = malloc(strlen(str) + 1);
    if (transformed == NULL) {
        // Handle memory allocation failure
        return NULL;
    }
    strcpy(transformed, str);
    for (int i = 0; transformed[i] != '\0'; i++) {
        transformed[i] = toupper(transformed[i]);
    }
    return transformed;
}

// Assume function del to free content of each node
void free_content(void *content) {
    free(content);
}

int main() {
    t_list_d *list = create_doubly_circular_linked_list(); // Assume this function creates a populated list
    
    // Mapping function to transform content to uppercase
    t_list_d *new_list = dc_lst_map(list, transform_content, free_content);
    
    if (new_list == NULL) {
        printf("Failed to create new list.\n");
        return 1;
    }
    
    // Use new_list
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Mapping and Creating New List**: The function creates a new doubly circular linked list by applying function `f` to each node's content of the input list `lst`.
2. **Transformation Function**: It uses the provided `f` function to transform each node's content.
3. **Memory Management**: If memory allocation fails during the creation of the new list, it uses `del` function to free the content of nodes.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
