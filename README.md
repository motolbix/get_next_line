*This project has been created as part of the 42 curriculum by motolbix.*

# Get Next Line

## Description

Get Next Line is a 42 School project that aims to develop a function capable of reading a file descriptor line by line.

The main goal of this project is to understand how file reading works in C, how to manage memory dynamically, and how to use static variables to preserve data between function calls.

The function returns one line at a time, including the newline character (`\n`) when it exists.

## Instructions

### Compilation

Compile the source files using:

```bash
cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c
```

`BUFFER_SIZE` determines the number of bytes read during each call to `read()`.

### Usage

Include the header file in your project:

```c
#include "get_next_line.h"
```

Call the function using a file descriptor:

```c
char *line;

line = get_next_line(fd);
```

Each call returns the next line from the file descriptor. It returns `NULL` when there is nothing left to read or when an error occurs.

## Features

- Reads a file descriptor line by line.
- Supports different `BUFFER_SIZE` values.
- Preserves remaining data between function calls using a static variable.
- Handles end-of-file (EOF).
- Supports multiple file descriptors in the bonus part.

## Resources

- 42 School Get Next Line subject.
- Linux manual pages: `read()`, `open()`, `close()`, `malloc()`, and `free()`.
- C programming documentation.

### AI Usage

AI was used to clarify C concepts related to static variables, file descriptors, system calls, the `read()` function, EOF, and kernel behavior. It was also used to better understand memory management and the expected behavior of the project functions.

