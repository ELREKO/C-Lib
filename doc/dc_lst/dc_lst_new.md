# dc_lst_new

## Description

The function **t_list_d *dc_lst_new(void *content)** creates a new node for a doubly circular linked list with the given `content`.

The `dc_lst_new` function allocates memory for a new node (`t_list_d`), initializes its `content` with the provided `content`, and sets the `next` and `prev` pointers to point to itself, making it a circular reference. It returns a pointer to the newly created node. If memory allocation fails, it returns `NULL`.

## Declaration
```c
t_list_d *dc_lst_new(void *content);
```
## Parameters

- **content**: The content to be stored in the new node.

## Return Value

- Returns a pointer to the newly created node (`t_list_d`).
- Returns `NULL` if memory allocation fails.

## Example

```c
#include "lib_main.h"

int main() {
    // Creating a new node with integer content
    int *data = malloc(sizeof(int));
    if (data == NULL) {
        perror("Failed to allocate memory");
        return 1;
    }
    *data = 42;
    
    t_list_d *new_node = dc_lst_new(data);
    
    if (new_node == NULL) {
        printf("Failed to create new node.\n");
        free(data);
        return 1;
    }
    
    // Use new_node
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Node Creation**: The function creates a new node for a doubly circular linked list with the given content.
2. **Memory Management**: It handles memory allocation for the new node and returns NULL if allocation fails.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
