# ft_split_single_quotes

## Description

The function **char **ft_split_single_quotes(char const *s, char c)** splits the string `s` into substrings based on the delimiter `c`, while also considering substrings enclosed within single quotes `'`.

The `ft_split_single_quotes` function allocates memory for an array of strings (`res`) to hold the resulting substrings. It calculates the number of substrings using `ft_split_num_substr_sq` and then uses `create_sub_str_sq` to populate `res` with each substring, considering both `c` as well as single quotes `'` as delimiters.

## Declaration

```c
char **ft_split_single_quotes(char const *s, char c);
```

## Parameters

- **s**: The string to be split into substrings.
- **c**: The delimiter character that separates substrings, except when inside single quotes `'`.

## Return Value

- Returns a dynamically allocated array of strings (`char **`) containing the substrings split from `s`.
- Returns `NULL` if memory allocation fails or if an error occurs during substring creation.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "abc def 'ghi jkl' mno";
    char c = ' ';

    char **res = ft_split_single_quotes(s, c);
    if (res) {
        for (int i = 0; res[i]; i++) {
            printf("Substring %d: %s\n", i + 1, res[i]);
        }
        // Output will be:
        // Substring 1: abc
        // Substring 2: def
        // Substring 3: ghi jkl
        // Substring 4: mno
    } else {
        printf("Error: Memory allocation failed\n");
    }

    // Clean up: Free all allocated memory
    if (res) {
        for (int i = 0; res[i]; i++) {
            free(res[i]);
        }
        free(res);
    }

    return 0;
}
```

## Usage

1. **Splitting Substrings**: The function splits the string `s` into substrings using the delimiter `c`, while also handling substrings enclosed within single quotes `'`.
2. **Memory Allocation**: It dynamically allocates memory for an array of strings (`res`) to store the resulting substrings.
3. **Error Handling**: It returns `NULL` if memory allocation fails or if an error occurs during substring creation.

---

# create_sub_str_sq

## Description

The static function **static int create_sub_str_sq(char **res, char const *s, char c)** populates the array `res` with substrings split from the string `s`, considering both `c` and single quotes `'` as delimiters.

The `create_sub_str_sq` function iterates through the string `s` character by character. It calls `inside_single_quotes` when encountering a single quote `'` at the beginning of a substring and `outside_single_quotes` otherwise to create each substring and store it in `res`.

## Declaration

```c
static int create_sub_str_sq(char **res, char const *s, char c);
```

## Parameters

- **res**: Pointer to a dynamically allocated array of strings (`char **`) where substrings will be stored.
- **s**: The string from which to extract substrings.
- **c**: The delimiter character that separates substrings, except when inside single quotes `'`.

## Return Value

- Returns `1` if all substrings are successfully created and stored in `res`.
- Returns `-1` if an error occurs during substring creation or memory allocation.

## Usage

1. **Populating Substrings**: The function populates the array `res` with substrings split from the string `s`, considering both `c` and single quotes `'` as delimiters.
2. **Error Handling**: It returns `-1` if an error occurs during substring creation or memory allocation.

---

# inside_single_quotes

## Description

The static function **static int inside_single_quotes(t_split_sq *data)** creates a substring from the string `data->s` starting at the current index `data->i_str`, considering it as enclosed within single quotes `'`.

The `inside_single_quotes` function is called by `create_sub_str_sq` when a single quote `'` is encountered at the beginning of a substring. It calculates the length of the substring using `get_substr_len` and allocates memory for `res[data->i_num_substr]` to store the substring.

## Declaration

```c
static int inside_single_quotes(t_split_sq *data);
```

## Parameters

- **data**: Pointer to a structure `t_split_sq` containing information about the current state of substring creation.

## Return Value

- Returns `1` if the substring within single quotes `'` is successfully created and stored in `res`.
- Returns `-1` if an error occurs during substring creation or memory allocation.

## Usage

1. **Handling Single Quotes**: The function handles cases where substrings are enclosed within single quotes `'` within the string `data->s`.
2. **Memory Allocation**: It allocates memory for `res[data->i_num_substr]` to store the substring within single quotes `'`.

---

# outside_single_quotes

## Description

The static function **static int outside_single_quotes(t_split_sq *data)** creates a substring from the string `data->s` starting at the current index `data->i_str`, considering it as not enclosed within single quotes `'`.

The `outside_single_quotes` function is called by `create_sub_str_sq` when a character that is not a single quote `'` or the delimiter `c` is encountered. It calculates the length of the substring using `get_substr_len` and allocates memory for `res[data->i_num_substr]` to store the substring.

## Declaration

```c
static int outside_single_quotes(t_split_sq *data);
```

## Parameters

- **data**: Pointer to a structure `t_split_sq` containing information about the current state of substring creation.

## Return Value

- Returns `1` if the substring outside single quotes `'` is successfully created and stored in `res`.
- Returns `-1` if an error occurs during substring creation or memory allocation.

## Usage

1. **Handling Substrings**: The function handles cases where substrings are not enclosed within single quotes `'` within the string `data->s`.
2. **Memory Allocation**: It allocates memory for `res[data->i_num_substr]` to store the substring outside single quotes `'`.

---

# get_substr_len

## Description

The static function **static int get_substr_len(char const *s, char c)** calculates the length of a substring in the string `s` starting from the current position and ending either at the next occurrence of `c` or at the end of the string.

The `get_substr_len` function is used by `inside_single_quotes` and `outside_single_quotes` to determine the length of the substring to be created and allocated in `res`.

## Declaration

```c
static int get_substr_len(char const *s, char c);
```

## Parameters

- **s**: The string from which to calculate the length of the substring.
- **c**: The delimiter character that marks the end of the substring.

## Return Value

- Returns the length of the substring starting from `s`.
- Returns `0` if `s` is `NULL` or if the substring length is `0`.

## Usage

1. **Calculating Substring Length**: The function calculates the length of a substring in the string `s` starting from the current position and ending at the next occurrence of `c` or at the end of the string.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
