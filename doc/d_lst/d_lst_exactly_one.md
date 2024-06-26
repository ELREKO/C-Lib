# d_lst_exactly_one

## Description

The function **int d_lst_exactly_one(t_list_d *lst_ptr)** checks if a doubly linked list has exactly one element.

The `d_lst_exactly_one` function checks the pointer `lst_ptr` to determine if it points to exactly one element in a doubly linked list. If `lst_ptr` is `NULL`, the function returns `0`. If `lst_ptr` points to exactly one element (i.e., the next pointer is `NULL`), the function returns `1`. Otherwise, it returns `0`.

## Declaration
```c
int d_lst_exactly_one(t_list_d *lst_ptr);
```
## Parameters

- **lst_ptr**: A pointer to the head of the doubly linked list (`t_list_d`).

## Return Value

- Returns `1` if the doubly linked list pointed to by `lst_ptr` has exactly one element.
- Returns `0` otherwise, including the case where `lst_ptr` is `NULL` or if there are zero or more than one elements.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list_with_single_element(); // Assume this function creates a list with exactly one element
    int result = d_lst_exactly_one(list);
    
    if (result == 1) {
        printf("The list has exactly one element.\n");
    } else {
        printf("The list does not have exactly one element.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Checking the List**: The function checks if the list pointed to by `lst_ptr` has exactly one element by examining the next pointer of the first element.
2. **Return Value**: It returns `1` if there is exactly one element, otherwise `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
