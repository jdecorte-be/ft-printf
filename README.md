<header>
<h1 align="center">
  <a href="https://github.com/jdecorte-be/ft-printf"><img src=".assets/banner.png" alt="ft-printf" ></a>
  ft-printf
  <br>
</h1>

<p align="center">
  A custom implementation of the C standard library's printf function. This project is part of the 42 school curriculum, handling various format specifiers.
</p>

<p align="center">
<a href="https://www.42.fr/">
    <img src="https://img.shields.io/badge/42-School%20Project-00b8d4?logo=42&logoColor=white&labelColor=000000"
         alt="42 School Project">
  </a>
<a href="#">
    <img src="https://img.shields.io/badge/Focus-Libc%20Re--implementation-555?logo=c&logoColor=white&labelColor=000000"
         alt="Focus Libc Re-implementation">
  </a>
<a href="#">
    <img src="https://img.shields.io/badge/Type-Static%20Library-blue?logo=books&logoColor=white&labelColor=000000"
         alt="Type Static Library">
  </a>
<a href="#">
    <img src="https://img.shields.io/badge/Standard-C99-A8B9CC?logo=c&logoColor=white&labelColor=000000"
         alt="Standard C99">
  </a>
</p>

<p align="center">
<a href="#">
    <img src="https://img.shields.io/badge/Platform-Linux%20%7C%20macOS-lightgrey?logo=linux&logoColor=white&labelColor=000000"
         alt="Platform Linux | macOS">
  </a>
  <a href="https://github.com/jdecorte-be/ft-printf/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/License-GPL--3.0-AE81FF?labelColor=000000"
         alt="ft-printf license">
  </a>
  <a href="https://github.com/jdecorte-be/ft-printf/stargazers">
    <img src="https://img.shields.io/github/stars/jdecorte-be/ft-printf?logo=star&logoColor=white&labelColor=000000&color=E6DB74"
         alt="ft-printf stars">
  </a>
  <a href="https://github.com/jdecorte-be/ft-printf/issues">
    <img src="https://img.shields.io/github/issues/jdecorte-be/ft-printf?logoColor=white&labelColor=000000&color=orange"
         alt="ft-printf issues">
  </a>
  <a href="https://github.com/jdecorte-be/ft-printf">
    <img src="https://img.shields.io/github/repo-size/jdecorte-be/ft-printf?logo=database&logoColor=white&labelColor=000000&color=AE81FF"
         alt="ft-printf repo size">
  </a>
  <a href="https://github.com/jdecorte-be/ft-printf">
    <img src="https://img.shields.io/github/languages/top/jdecorte-be/ft-printf?logo=code&logoColor=white&labelColor=000000&color=A6E22E"
         alt="ft-printf top language">
  </a>
</p>
<p align="center">
  <a href="#ftprintf">Ft_printf</a> •
  <a href="#some-examples">Some examples</a> •
  <a href="#output">Output:</a>
</p>
</header>


A custom implementation of the C standard library's `printf` function. This project is part of the 42 school curriculum and recodes the original `printf` behavior, providing a lightweight and portable way to format and print data.

## Features

This implementation of `ft_printf` supports the following format specifiers, flags, and features:

#### Conversion Specifiers

| Specifier | Output |
| :---: | --- |
| `%c` | A single character. |
| `%s` | A string of characters. |
| `%p` | The memory address of a pointer, in hexadecimal format. |
| `%d` | A signed decimal integer. |
| `%i` | A signed decimal integer. |
| `%u` | An unsigned decimal integer. |
| `%x` | An unsigned hexadecimal integer (lowercase). |
| `%X` | An unsigned hexadecimal integer (uppercase). |
| `%%` | A literal percent sign (`%`). |

#### Flags and Modifiers

-   **`-`**: Left-justify the output within the field width.
-   **`0`**: Zero-pad the output instead of using spaces.
-   **`.`**: Specifies precision for strings and integers.
-   **`#`**: Alternate form; prepends `0x` or `0X` for hexadecimal conversions.
-   **Width**: Specifies a minimum field width for the output.
-   **`*`**: Use the next argument as the field width.

## Getting Started

### Prerequisites

-   A C compiler (e.g., `gcc` or `clang`)
-   `make` build automation tool

### Building the Library

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/jdecorte-be/ft-printf.git
    cd ft-printf
    ```

2.  **Compile the source files:**
    Run `make` to compile the project and create the static library `libftprintf.a`.
    ```sh
    make
    ```

## Usage

To use `ft_printf` in your C project, include the header and link against the compiled library.

1.  Include the header file in your source code: `#include "ft_printf.h"`.
2.  Compile your project, linking the `libftprintf.a` library.

### Example

Here is a simple `main.c` demonstrating the function's usage:

```c
#include "includes/ft_printf.h"

int main(void)
{
    char *str = "world";
    int   num = 42;
    int   char_count;

    ft_printf("--- Testing ft_printf ---\n");
    ft_printf("Hello, %s!\n", str);
    ft_printf("The answer is %d.\n", num);
    ft_printf("Hexadecimal for %d is %#x.\n", num, num);
    ft_printf("Pointer address: %p\n", &num);

    char_count = ft_printf("This line has %d characters.\n", 31);
    ft_printf("The previous line printed %d characters.\n", char_count);

    return (0);
}
```

#### Compiling and Running

First, ensure `libftprintf.a` has been created by running `make`. Then, compile your `main.c` with the library:

```sh
# Compile the main program and link the library
gcc main.c -L. -lftprintf -Iincludes -o example

# Run the executable
./example
```

#### Expected Output

```
--- Testing ft_printf ---
Hello, world!
The answer is 42.
Hexadecimal for 42 is 0x2a.
Pointer address: 0x7ff7bfeff22c
This line has 31 characters.
The previous line printed 31 characters.
```
*Note: The pointer address will vary on your system.*

## License

This project is licensed under the terms specified in the `LICENSE` file.
