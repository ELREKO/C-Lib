# dc_lst_print_sep

## Description

The function **void dc_lst_print_sep(void)** prints a separator line using colored formatting.

The `dc_lst_print_sep` function uses `ft_printf` to print a green-colored separator line consisting of asterisks (`*`). It then resets the text color to white before returning. This function assumes that the macros `GREEN` and `WHITE` are defined elsewhere in the program, likely specifying ANSI color codes for terminal output.

## Declaration
```c
void dc_lst_print_sep(void);
```
## Parameters

This function does not take any parameters.

## Return Value

This function does not return a value (`void`).

## Example
```c
#include "lib_main.h"

// Assume GREEN and WHITE are defined macros in lib_main.h

int main() {
    dc_lst_print_sep();
    return 0;
}
```
## Usage

1. **Separator Printing**: It uses `ft_printf` to print a green-colored line of asterisks (`*`) to serve as a visual separator.
2. **Color Reset**: It ensures that text color is reset to white (`WHITE`) after printing the separator.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
