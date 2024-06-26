# ft_putnbr_base_check

## Description

The function **size_t ft_putnbr_base_check(const char *base, t_base_info *base_info)** checks if the given base is valid for numeric conversions and updates the `base_info` structure accordingly.

The `ft_putnbr_base_check` function validates the provided base string to ensure it can be used for base conversions. It checks the length of the base, ensures there are no invalid characters (`+` or `-`), and verifies that there are no duplicate characters in the base.

## Declaration

size_t ft_putnbr_base_check(const char *base, t_base_info *base_info);

## Parameters

- **base**: A pointer to the string representing the base to be checked.
- **base_info**: A pointer to the `t_base_info` structure where the base information will be stored if the base is valid.

## Return Value

This function returns `1` if the base is valid, and `0` if the base is invalid.

## Example

```c
#include "lib_main.h"

int main() {
    t_base_info base_info;
    const char *base = "0123456789ABCDEF"; // Hexadecimal base

    if (ft_putnbr_base_check(base, &base_info)) {
        printf("Base is valid. Base length: %zu\n", base_info.base_len);
    } else {
        printf("Base is invalid.\n");
    }

    return 0;
}
```

## Internal Functions

### ft_strlen

```c
size_t ft_strlen(const char *s);
```
The `ft_strlen` function computes the length of the string `s`.

### ft_str_cont_chars

```c
int ft_str_cont_chars(const char *s, const char *chars);
```
The `ft_str_cont_chars` function checks if any of the characters in `chars` are present in the string `s`.

### ft_str_cont_duplic

```c
int ft_str_cont_duplic(const char *s);
```
The `ft_str_cont_duplic` function checks if there are any duplicate characters in the string `s`.

## Usage

1. **Base Length Check**: It checks if the base length is greater than 1.
2. **Invalid Character Check**: It verifies that the base does not contain `+` or `-` characters.
3. **Duplicate Character Check**: It ensures there are no duplicate characters in the base.
4. **Base Information Update**: If the base is valid, it updates the `base_info` structure with the base string and its length.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
