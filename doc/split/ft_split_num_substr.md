# ft_split_num_substr

## Description

The function **size_t ft_split_num_substr(char const *s, char c)** calculates the number of substrings delimited by the character `c` in the string `s`.

The `ft_split_num_substr` function iterates through the string `s` character by character. It counts substrings whenever it encounters a character that is not `c` and transitions `state` from `0` to `1`. It resets `state` to `0` when encountering `c` after previously being in a substring.

## Declaration

```c
size_t ft_split_num_substr(char const *s, char c);
```

## Parameters

- **s**: The string in which substrings are counted.
- **c**: The delimiter character that separates substrings.

## Return Value

- Returns the number of substrings in the string `s` delimited by the character `c`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "abc def ghi";
    char c = ' ';

    size_t num_substr = ft_split_num_substr(s, c);
    printf("Number of substrings: %zu\n", num_substr); // Output will be "3"

    return 0;
}
```

## Usage

1. **Counting Substrings**: The function counts the number of substrings in the string `s` using the delimiter `c`.
2. **Handling Edge Cases**: It correctly handles cases where `s` starts or ends with `c`, or has consecutive `c` characters.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
