# ft_split_str

## Description

The function **char **ft_split_str(char const *s, char const *split_at)** splits the string `s` into substrings based on the delimiter `split_at`.

The `ft_split_str` function allocates memory for an array of strings (`res`) to hold the resulting substrings. It calculates the number of substrings using `calc_num_substr` and then uses `create_sub_str` to populate `res` with each substring.

## Declaration

```c
char **ft_split_str(char const *s, char const *split_at);
```

## Parameters

- **s**: The string to be split into substrings.
- **split_at**: The delimiter string that marks the boundaries of substrings.

## Return Value

- Returns a dynamically allocated array of strings (`char **`) containing the substrings split from `s`.
- Returns `NULL` if memory allocation fails or if an error occurs during substring creation.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "apple,orange,banana";
    char const *split_at = ",";

    char **res = ft_split_str(s, split_at);
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

1. **Splitting Substrings**: The function splits the string `s` into substrings using the delimiter `split_at`.
2. **Memory Allocation**: It dynamically allocates memory for an array of strings (`res`) to store the resulting substrings.
3. **Error Handling**: It returns `NULL` if memory allocation fails or if an error occurs during substring creation.

---

# create_sub_str

## Description

The static function **static int create_sub_str(char **res, char const *s, char const *split_at, size_t split_at_length)** populates the array `res` with substrings split from the string `s`, using the delimiter `split_at`.

The `create_sub_str` function iterates through the string `s` character by character. It calls `get_substr_len` to calculate the length of each substring and allocates memory for `res[i_num_substr]` to store each substring.

## Declaration

```c
static int create_sub_str(char **res, char const *s, char const *split_at, size_t split_at_length);
```

## Parameters

- **res**: Pointer to a dynamically allocated array of strings (`char **`) where substrings will be stored.
- **s**: The string from which to extract substrings.
- **split_at**: The delimiter string that marks the boundaries of substrings.
- **split_at_length**: The length of the delimiter string `split_at`.

## Return Value

- Returns `1` if all substrings are successfully created and stored in `res`.
- Returns `0` if memory allocation fails or if an error occurs during substring creation.

## Usage

1. **Populating Substrings**: The function populates the array `res` with substrings split from the string `s` using the delimiter `split_at`.
2. **Memory Allocation**: It allocates memory for `res[i_num_substr]` to store each substring.
3. **Error Handling**: It returns `0` if memory allocation fails or if an error occurs during substring creation.

---

# get_substr_len

## Description

The static function **static int get_substr_len(char const *s, char const *split_at, size_t split_at_length)** calculates the length of a substring in the string `s` starting from the current position, until it encounters the delimiter `split_at`.

The `get_substr_len` function is used by `create_sub_str` to determine the length of each substring to be created and allocated in `res`.

## Declaration

```c
static int get_substr_len(char const *s, char const *split_at, size_t split_at_length);
```

## Parameters

- **s**: The string from which to calculate the length of the substring.
- **split_at**: The delimiter string that marks the end of the substring.
- **split_at_length**: The length of the delimiter string `split_at`.

## Return Value

- Returns the length of the substring starting from `s` until it encounters the delimiter `split_at`.
- Returns `0` if `s` is `NULL` or if the substring length is `0`.

## Usage

1. **Calculating Substring Length**: The function calculates the length of a substring in the string `s` starting from the current position, until it encounters the delimiter `split_at`.

---

# calc_num_substr

## Description

The static function **static size_t calc_num_substr(char const *s, char const *split_at, size_t *num_substr, size_t split_at_length)** calculates the number of substrings in the string `s` based on the delimiter `split_at`.

The `calc_num_substr` function iterates through the string `s` character by character. It increments the count `num_substr` each time it finds a substring not delimited by `split_at`.

## Declaration

```c
static size_t calc_num_substr(char const *s, char const *split_at, size_t *num_substr, size_t split_at_length);
```

## Parameters

- **s**: The string in which to count the number of substrings.
- **split_at**: The delimiter string that marks the boundaries of substrings.
- **num_substr**: Pointer to a variable holding the current count of substrings.
- **split_at_length**: The length of the delimiter string `split_at`.

## Return Value

- Returns the total number of substrings found in the string `s` based on the delimiter `split_at`.

## Usage

1. **Counting Substrings**: The function counts the number of substrings in the string `s` based on the delimiter `split_at`.
2. **Incrementing Count**: It increments `num_substr` each time it finds a substring not delimited by `split_at`.

---

# split_at_occurs

## Description

The static function **static int split_at_occurs(char const *str, char const *split_at, size_t split_at_length)** checks if the delimiter `split_at` occurs at the current position in the string `str`.

The `split_at_occurs` function compares the substring of `str` with `split_at` to determine if they are equal.

## Declaration

```c
static int split_at_occurs(char const *str, char const *split_at, size_t split_at_length);
```

## Parameters

- **str**: The string in which to check for the occurrence of the delimiter `split_at`.
- **split_at**: The delimiter string to check against `str`.
- **split_at_length**: The length of the delimiter string `split_at`.

## Return Value

- Returns `1` if the delimiter `split_at` occurs at the current position in `str`.
- Returns `0` otherwise.

## Usage

1. **Checking Delimiter Occurrence**: The function checks if the delimiter `split_at` occurs at the current position in the string `str`.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
