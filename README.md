LibMX
LibMX is a C library designed to offer a collection of useful functions for various common programming tasks. It includes utilities for handling strings, memory operations, linked lists, and more.

Features

Linked List Operations
mx_create_node: Create a new node in a linked list.
mx_push_front: Insert a node at the beginning of the list.
mx_push_back: Append a node to the end of the list.
mx_pop_front: Remove the first node from the list.
mx_pop_back: Remove the last node from the list.
mx_list_size: Get the number of nodes in the list.
mx_sort_list: Sort the linked list elements.
String Utilities
mx_strlen: Get the length of a string.
mx_strcpy: Copy a string.
mx_strncpy: Copy part of a string.
mx_strcat: Concatenate two strings.
mx_strdup: Duplicate a string.
mx_strndup: Duplicate the first n characters of a string.
mx_strtrim: Trim whitespace from the beginning and end of a string.
mx_strsplit: Split a string into an array of substrings.
mx_strjoin: Join two strings.
mx_replace_substr: Replace a substring with another substring.
mx_count_words: Count the number of words in a string.
Memory Operations
mx_memcpy: Copy memory blocks.
mx_memset: Set memory blocks to a specific value.
mx_memccpy: Copy memory until a specified character is found.
mx_memchr: Locate the first occurrence of a character in a memory block.
mx_memcmp: Compare memory blocks.
mx_memmove: Move memory blocks.
mx_realloc: Resize a memory block.
Mathematical Functions
mx_pow: Calculate the power of a number.
mx_sqrt: Calculate the square root of a number.
I/O Functions
mx_read_line: Read a line from a file descriptor.
Utilities
mx_printchar: Print a character to the standard output.
mx_print_unicode: Print a Unicode character.
mx_printstr: Print a string.
mx_print_strarr: Print an array of strings.
mx_printint: Print an integer.
mx_file_to_str: Read the contents of a file into a string.
Installation

To use this library, clone the repository and include the header file libmx.h in your project. Compile your code with the source files provided in this repository.

bash
Copy code
git clone <repository_url>
Usage

Include the header file in your C source code:

c
Copy code
#include "libmx.h"
Compile your project, linking against the library:

bash
Copy code
gcc -o your_program your_program.c -L/path/to/libmx -lmx
Examples

Creating and Manipulating a Linked List
c
Copy code
#include "libmx.h"
#include <stdio.h>

int main() {
    t_list *list = NULL;

    mx_push_front(&list, "First");
    mx_push_back(&list, "Second");
    mx_push_back(&list, "Third");

    printf("List size: %d\n", mx_list_size(list));

    mx_pop_front(&list);
    mx_pop_back(&list);

    printf("List size after popping: %d\n", mx_list_size(list));

    // Free remaining nodes
    while (list != NULL) {
        mx_pop_front(&list);
    }

    return 0;
}
