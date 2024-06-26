# ft_pow

## Description

The function **int ft_pow(int nb, int power)** computes the power of an integer **nb** raised to the **power**.

## Declaration

```c
int ft_pow(int nb, int power);
```

## Parameters

- **nb**: The base integer.
- **power**: The exponent integer.

## Return Value

- The result of **nb** raised to the power of **power**. If **power** is less than 0, the function returns 0.

## Example

```c
#include "lib_main.h"

int main() {
    int base = 2;
    int exponent1 = 3;
    int exponent2 = -2;
    
    int result1 = ft_pow(base, exponent1);
    int result2 = ft_pow(base, exponent2);
    
    ft_printf("%d raised to the power of %d is %d\n", base, exponent1, result1);
    ft_printf("%d raised to the power of %d is %d\n", base, exponent2, result2);
    
    return 0;
}
```

## Usage

1. **Non-negative Exponent**: If **power** is 0 or greater, the function computes **nb** raised to **power** using recursion.
2. **Negative Exponent**: If **power** is less than 0, the function returns 0.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
