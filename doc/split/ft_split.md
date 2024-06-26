# ft_split

## Description

The function **char **ft_split(char const *s, char c)** splits the string `s` into substrings based on the delimiter `c`.

The `ft_split` function allocates memory for an array of strings (`res`) to hold the resulting substrings. It calculates the number of substrings using `ft_split_num_substr` and then uses `create_sub_str` to populate `res` with each substring.

## Declaration

```c
char **ft_split(char const *s, char c);
```

## Parameters

- **s**: The string to be split into substrings.
- **c**: The delimiter character that marks the boundaries of substrings.

## Return Value

- Returns a dynamically allocated array of strings (`char **`) containing the substrings split from `s`.
- Returns `NULL` if memory allocation fails or if an error occurs during substring creation.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "apple,orange,banana";
    char c = ',';

    char **res = ft_split(s, c);
    if (res) {
        for (int i = 0; res[i]; i++) {
            printf("Substring %d: %s\n", i + 1, res[i]);
        }
        // Output will be:
        // Substring 1: apple
        // Substring 2: orange
        // Substring 3: banana
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

1. **Splitting Substrings**: The function splits the string `s` into substrings using the delimiter `c`.
2. **Memory Allocation**: It dynamically allocates memory for an array of strings (`res`) to store the resulting substrings.
3. **Error Handling**: It returns `NULL` if memory allocation fails or if an error occurs during substring creation.

---

# create_sub_str

## Description

The static function **static int create_sub_str(char **res, char const *s, char c)** populates the array `res` with substrings split from the string `s`, using the delimiter `c`.

The `create_sub_str` function iterates through the string `s` character by character. It calls `get_substr_len` to calculate the length of each substring and allocates memory for `res[i_num_substr]` to store each substring.

## Declaration

```c
static int create_sub_str(char **res, char const *s, char c);
```

## Parameters

- **res**: Pointer to a dynamically allocated array of strings (`char **`) where substrings will be stored.
- **s**: The string from which to extract substrings.
- **c**: The delimiter character that marks the boundaries of substrings.

## Return Value

- Returns `1` if all substrings are successfully created and stored in `res`.
- Returns `0` if memory allocation fails or if an error occurs during substring creation.

## Usage

1. **Populating Substrings**: The function populates the array `res` with substrings split from the string `s` using the delimiter `c`.
2. **Memory Allocation**: It allocates memory for `res[i_num_substr]` to store each substring.
3. **Error Handling**: It returns `0` if memory allocation fails or if an error occurs during substring creation.

---

# get_substr_len

## Description

The static function **static int get_substr_len(char const *s, char c)** calculates the length of a substring in the string `s` starting from the current position, until it encounters the delimiter `c`.

The `get_substr_len` function is used by `create_sub_str` to determine the length of each substring to be created and allocated in `res`.

## Declaration

```c
static int get_substr_len(char const *s, char c);
```

## Parameters

- **s**: The string from which to calculate the length of the substring.
- **c**: The delimiter character that marks the end of the substring.

## Return Value

- Returns the length of the substring starting from `s` until it encounters the delimiter `c`.
- Returns `0` if `s` is `NULL` or if the substring length is `0`.

## Usage

1. **Calculating Substring Length**: The function calculates the length of a substring in the string `s` starting from the current position, until it encounters the delimiter `c`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
