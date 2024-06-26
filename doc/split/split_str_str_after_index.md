# split_str_str_after_index

## Description

The function **int split_str_str_after_index(char const *s, char const *split_at, char ***res, int index)** splits the string `s` starting from the specified `index` after finding the substring `split_at`.

The function allocates memory for an array of strings (`res`) to hold the substrings resulting from the split operation. It checks for empty strings using `str_is_empty` and handles special cases accordingly. It uses helper functions `dup_otherwise_empty`, `ft_str_n_dup_int`, and `free_res` for memory allocation and management.

## Declaration

```c
int split_str_str_after_index(char const *s, char const *split_at, char ***res, int index);
```

## Parameters

- **s**: The string to be split.
- **split_at**: The substring used as a delimiter to split `s`.
- **res**: A pointer to a dynamically allocated array of strings (`char **`) that will store the resulting substrings.
- **index**: The starting index in `s` from which to begin the split operation.

## Return Value

- Returns `0` if the split operation is successful.
- Returns `1` if memory allocation fails for `res`.
- Returns `4` if memory allocation fails for the first substring.
- Returns `5` if memory allocation fails for the second substring.
- Returns `6` if both `s` and `split_at` are empty strings.

## Example

```c
#include "lib_main.h"
#include <stdio.h>

int main() {
    char const *s = "hello_world_example";
    char const *split_at = "_";
    char **res = NULL;
    int index = 5;

    int result = split_str_str_after_index(s, split_at, &res, index);
    if (result == 0) {
        printf("First substring: %s\n", res[0]);
        printf("Second substring: %s\n", res[1]);
    } else {
        printf("Error: Split operation failed with code %d\n", result);
    }

    // Clean up: Free all allocated memory
    if (res) {
        free(res[0]);
        free(res[1]);
        free(res);
    }

    return 0;
}
```

## Usage

1. **Splitting Strings**: The function splits the string `s` starting from the specified `index` after finding the substring `split_at`.
2. **Memory Allocation**: It dynamically allocates memory for an array of strings (`res`) to store the resulting substrings.
3. **Error Handling**: It returns specific error codes (`1`, `4`, `5`, `6`) if memory allocation fails or if `s` and `split_at` are empty strings.

---

# handle_empty_strings

## Description

The static function **static int handle_empty_strings(char const *s, char const *split_at, char ***res)** handles special cases where either `s`, `split_at`, or both are empty strings during the split operation in `split_str_str_after_index`.

The function checks for empty strings using `str_is_empty` and returns specific error codes or performs appropriate actions based on the conditions.

## Declaration

```c
static int handle_empty_strings(char const *s, char const *split_at, char ***res);
```

## Parameters

- **s**: The string to be split.
- **split_at**: The substring used as a delimiter to split `s`.
- **res**: A pointer to a dynamically allocated array of strings (`char **`) that will store the resulting substrings.

## Return Value

- Returns `0` if handling of empty strings is successful.
- Returns `6` if both `s` and `split_at` are empty strings.

## Usage

1. **Handling Empty Strings**: The function handles cases where `s`, `split_at`, or both are empty strings during the split operation.
2. **Error Handling**: It returns specific error codes (`6`) if both `s` and `split_at` are empty strings.

---

# dup_otherwise_empty

## Description

The static function **static int dup_otherwise_empty(char ***res, char const *str1, char const *str2)** duplicates the strings `str1` and `str2` into the array `res`, or assigns empty strings if `str1` or `str2` is `NULL`.

The function is used by `split_str_str_after_index` to handle cases where one of the substrings (`str1` or `str2`) may be `NULL` or empty.

## Declaration

```c
static int dup_otherwise_empty(char ***res, char const *str1, char const *str2);
```

## Parameters

- **res**: A pointer to a dynamically allocated array of strings (`char **`) where substrings will be stored.
- **str1**: The first string to be duplicated into `res[0]`.
- **str2**: The second string to be duplicated into `res[1]`.

## Return Value

- Returns `0` if both strings (`str1` and `str2`) are successfully duplicated or assigned as empty strings into `res`.
- Returns `2` if memory allocation fails for `str1`.
- Returns `3` if memory allocation fails for `str2`.

## Usage

1. **Duplicating Strings**: The function duplicates `str1` and `str2` into the array `res`, or assigns empty strings if `str1` or `str2` is `NULL`.
2. **Memory Allocation**: It returns specific error codes (`2`, `3`) if memory allocation fails for `str1` or `str2`.

---

# free_res

## Description

The static function **static int free_res(char ***res, int ret_code, int free_what)** frees the allocated memory for the array `res` and optionally for the strings stored in `res`.

The function is used by `split_str_str_after_index` to free memory in case of errors during the split operation or after successfully handling empty strings.

## Declaration

```c
static int free_res(char ***res, int ret_code, int free_what);
```

## Parameters

- **res**: A pointer to a dynamically allocated array of strings (`char **`) where substrings are stored.
- **ret_code**: The return code to be returned by the function.
- **free_what**: Determines whether to free the strings (`0` - free both strings, `1` - free only the second string).

## Return Value

- Returns `ret_code` passed to the function.
- Frees the allocated memory for `res` and optionally for the strings stored in `res`.

## Usage

1. **Freeing Memory**: The function frees the allocated memory for the array `res` and optionally for the strings stored in `res`.
2. **Error Handling**: It returns `ret_code` passed to the function after freeing the memory.

---

- [Back to overview](../Overview_about_function.md)
- [Back to main](/)
