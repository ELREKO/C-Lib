# ft_abs

## Description

The function **int ft_abs(int nb)** computes the absolute value of an integer **nb**.

## Declaration

```c
int ft_abs(int nb);
```

## Parameters

- **nb**: The integer for which the absolute value is to be computed.

## Return Value

- The absolute value of **nb**.

## Example

```c
#include "lib_main.h"

int main() {
    int num1 = -10;
    int num2 = 20;
    
    int abs_num1 = ft_abs(num1);
    int abs_num2 = ft_abs(num2);
    
    ft_printf("Absolute value of %d is %d\n", num1, abs_num1);
    ft_printf("Absolute value of %d is %d\n", num2, abs_num2);
    
    return 0;
}
```

## Usage

1. **Negative Input**: If **nb** is less than 0, the function returns **nb** multiplied by -1.
2. **Non-negative Input**: If **nb** is greater than or equal to 0, the function returns **nb** itself.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
