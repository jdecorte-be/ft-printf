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

Recoding the libc’s printf function!

##### Status
 - Mandatory part Finished 100%
 
### Some examples
```C
int main(void)
{
    ft_printf("26----------------------\n");
    printf("%d\n",    printf("   printf |%-8.6d|%-8.6d|\n", 1025, -1025));
    printf("%d\n", ft_printf("ft_printf |%-8.6d|%-8.6d|\n", 1025, -1025));
    ft_printf("26----------------------\n");
    printf("%d\n",    printf("   printf |%-15.8d|\n", 15));
    printf("%d\n", ft_printf("ft_printf |%-15.8d|\n", 15));
    ft_printf("26----------------------\n");
    printf("%d\n",    printf("|%-20.8d|\n", 15));
    printf("%d\n", ft_printf("|%-20.8d|\n", 15));
    ft_printf ("111-----------------------------------\n");
    printf("%d\n",    printf("   printf |%0*d|%0*d|\n",  -3, 10012, -3, -10012));
    printf("%d\n", ft_printf("ft_printf |%0*d|%0*d|\n",  -3, 10012, -3, -10012));
    ft_printf ("119-----------------------------------\n");
    printf("%d\n",    printf("   printf |%-*d|%-*d|\n",  5, 10012, 5, -10012));
    printf("%d\n", ft_printf("ft_printf |%-*d|%-*d|\n",  5, 10012, 5, -10012));
    return (0);
}
```
### Output:
```Shell
./a.out 
26------------------------------------
   printf |001025  |-001025 | 30
ft_printf |001025  |-001025 | 30
26------------------------------------
   printf |00000015       | 28
ft_printf |00000015       | 28
26------------------------------------
|00000015            | 23
|00000015            | 23
111-----------------------------------
   printf |10012|-10012| 25
ft_printf |10012|-10012| 25
119-----------------------------------
   printf |10012|-10012| 25
ft_printf |10012|-10012| 25
```
