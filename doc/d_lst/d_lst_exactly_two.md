# d_lst_exactly_two

## Description

The function **int d_lst_exactly_two(t_list_d *lst_ptr)** checks if a doubly linked list has exactly two elements.

The `d_lst_exactly_two` function examines the doubly linked list starting from `lst_ptr` to determine if it contains exactly two elements. If `lst_ptr` is `NULL` or points to less than two elements, the function returns `0`. If `lst_ptr` points to exactly two elements, the function returns `1`. Otherwise, it returns `0`.

## Declaration
```c
int d_lst_exactly_two(t_list_d *lst_ptr);
```
## Parameters

- **lst_ptr**: A pointer to the head of the doubly linked list (`t_list_d`).

## Return Value

- Returns `1` if the doubly linked list pointed to by `lst_ptr` has exactly two elements.
- Returns `0` otherwise, including the case where `lst_ptr` is `NULL` or if there are fewer or more than two elements.

## Example

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list_with_two_elements(); // Assume this function creates a list with exactly two elements
    int result = d_lst_exactly_two(list);
    
    if (result == 1) {
        printf("The list has exactly two elements.\n");
    } else {
        printf("The list does not have exactly two elements.\n");
    }
    
    return 0;
}
```
## Internal Functions

None

### Usage

1. **Checking the List**: The function checks if the list pointed to by `lst_ptr` has exactly two elements by examining the next pointers of the first and second elements.
2. **Return Value**: It returns `1` if there are exactly two elements, otherwise `0`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
