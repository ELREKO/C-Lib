# ft_split_num_substr_sq

## Description

The function **size_t ft_split_num_substr_sq(char const *s, char c)** calculates the number of substrings delimited by the character `c` in the string `s`, while also considering substrings enclosed within single quotes `'`.

The `ft_split_num_substr_sq` function iterates through the string `s` character by character. It counts substrings separated by `c`, except when `c` is inside single quotes. It uses the helper function `inside_single_quotes` to handle cases where `c` is encountered within single quotes. 

## Declaration

```c
size_t ft_split_num_substr_sq(char const *s, char c);
```

## Parameters

- **s**: The string in which substrings are counted.
- **c**: The delimiter character that separates substrings, except when inside single quotes.

## Return Value

- Returns the number of substrings in the string `s`, considering single quotes as delimiters for `c`.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "abc def 'ghi jkl' mno";
    char c = ' ';

    size_t num_substr = ft_split_num_substr_sq(s, c);
    printf("Number of substrings: %zu\n", num_substr); // Output will be "3"

    return 0;
}
```

## Usage

1. **Counting Substrings**: The function counts the number of substrings in the string `s`, considering both the delimiter `c` and single quotes as delimiters for `c`.
2. **Handling Edge Cases**: It handles cases where `c` is inside single quotes by using the helper function `inside_single_quotes`.

---

## inside_single_quotes

### Description

The static function **static int inside_single_quotes(char const *s, int *i, size_t *num_substr)** checks if the current position `*i` in the string `s` is inside single quotes `'`.

The `inside_single_quotes` function is called by `ft_split_num_substr_sq` when a single quote `'` is encountered. It increments `*i` to skip the initial single quote and counts a new substring within single quotes until another single quote `'` is encountered or the end of the string `s` is reached.

### Declaration

```c
static int inside_single_quotes(char const *s, int *i, size_t *num_substr);
```

### Parameters

- **s**: The string in which to check for single quotes.
- **i**: Pointer to the current index in the string `s`.
- **num_substr**: Pointer to the counter of substrings.

### Return Value

- Returns `1` if the end of the string `s` is reached while inside single quotes.
- Returns `0` otherwise.

### Example

```c
// This function is not directly invoked by user code; it is called internally by ft_split_num_substr_sq.
```

## Usage

1. **Handling Single Quotes**: The function handles cases where substrings are enclosed within single quotes within the string `s`.
2. **Incrementing Index**: It increments the index `*i` to skip over the substring within single quotes.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
