# ft_striteri

## Description

The function **void ft_striteri(char *s, void (*f)(unsigned int, char *))** applies the function `f` to each character of the string `s`, passing its index as the first argument to `f`.

## Declaration

```c
void ft_striteri(char *s, void (*f)(unsigned int, char *));
```

## Parameters

- **s**: The string to iterate over (`char *`).
- **f**: The function to apply to each character. It takes two parameters:
  - `unsigned int`: The index of the current character.
  - `char *`: A pointer to the current character.

## Return Value

- **void**: The function does not return a value.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

// Example function to print the index and character
void print_index_char(unsigned int index, char *c) {
    printf("Character at index %u: %c\n", index, *c);
}

int main() {
    char str[] = "Hello";

    ft_striteri(str, print_index_char);

    return 0;
}
```

## Usage

1. **Iteration**: Iterates over each character in the string `s`.
2. **Function Application**: Applies the function `f` to each character, passing the index and a pointer to the character.
3. **Custom Function**: `f` can be any function that accepts an `unsigned int` index and a `char *` pointer.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
