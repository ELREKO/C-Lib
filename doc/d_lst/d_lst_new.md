# d_lst_new

## Description

The function **t_list_d *d_lst_new(void *content)** creates a new doubly linked list node (`t_list_d`) with the given content.

The `d_lst_new` function allocates memory for a new doubly linked list node, initializes its `content` with the provided parameter `content`, and sets its `prev` and `next` pointers to `NULL`. If memory allocation fails, the function returns `NULL`.

## Declaration
```c
t_list_d *d_lst_new(void *content);
```
## Parameters

- **content**: A pointer to the content that the new node (`t_list_d`) will hold.

## Return Value

- Returns a pointer to the newly created doubly linked list node (`t_list_d`).
- Returns `NULL` if memory allocation fails.

## Example

```c
#include "lib_main.h"

int main() {
    // Example to create a new node with an integer content
    int *data = malloc(sizeof(int));
    if (data == NULL) {
        perror("Failed to allocate memory");
        return 1;
    }
    *data = 42;
    
    t_list_d *new_node = d_lst_new(data);
    if (new_node != NULL) {
        printf("New node created successfully.\n");
        printf("Node content: %d\n", *(int *)new_node->content);
        free(data); // Remember to free allocated memory after use
        free(new_node); // Remember to free the node itself
    } else {
        printf("Failed to create a new node.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Creating a New Node**: The function creates a new doubly linked list node (`t_list_d`) with the provided content.
2. **Memory Allocation**: It handles memory allocation internally and returns `NULL` if allocation fails.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
