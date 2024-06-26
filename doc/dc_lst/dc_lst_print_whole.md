# dc_lst_print_whole

## Description

The function **void dc_lst_print_whole(t_list_d *lst_ptr, const char *longShort, const char *type)** prints the contents of a doubly linked list based on specified printing criteria.

The `dc_lst_print_whole` function takes a pointer to the head node of a doubly linked list (`lst_ptr`), a string indicating whether to print in "long" or "short" format (`longShort`), and a string specifying the data type ("int" or "str") to print (`type`). Depending on the values of `longShort` and `type`, it calls internal functions (`print_long` or `print_short`) to iterate through the list and print either detailed or concise information about each node.

## Declaration

void dc_lst_print_whole(t_list_d *lst_ptr, const char *longShort, const char *type);

## Parameters

- **lst_ptr**: Pointer to the head node (`t_list_d`) of the doubly linked list to print.
- **longShort**: String indicating whether to print in "long" or "short" format.
- **type**: String specifying the data type ("int" or "str") to print.

## Return Value

This function does not return a value (`void`).

## Example

Assume `t_list_d`, `dc_lst_print_one_int_short`, `dc_lst_print_one_str_short`, `dc_lst_print_one_int_long`, and `dc_lst_print_one_str_long` are defined in `lib_main.h`.

```c
#include "lib_main.h"

int main() {
    t_list_d *list = create_doubly_linked_list(); // Assume function to create list
    dc_lst_print_whole(list, "short", "int");
    return 0;
}
```

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
