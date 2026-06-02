# 🖨️ ft_printf

A 42 project reimplementing the C standard `printf` function from scratch.

---

## Introduction

`ft_printf` is a recoded version of the standard C `printf` function.  
The goal is to understand how **variadic functions** work and how to handle **format specifiers** manually.

### Key Concepts

- **Variadic functions** — functions that accept a variable number of arguments with `va_list`, `va_start`, `va_arg`, `va_end`
- **Format parsing** — reading a format string and identifying conversion specifiers
- **Type handling** — casting and printing different data types correctly

---

## ⚙️ Usage

### Compilation

```bash
make        # Compile the library
make clean  # Remove object files
make fclean # Remove object files and library
make re     # Full recompilation
```

`ft_printf` compiles into a **static library** `libftprintf.a`.  
To use it in your own project, include the header and link the library at compilation :

```bash
cc main.c libftprintf.a -o program
```

### In your code

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s! You are %d years old.\n", "Name", 42);
    return (0);
}
```

---

## Supported Conversions

| Specifier | Description |
|---|---|
| `%c` | Single character |
| `%s` | String |
| `%p` | Pointer address in hexadecimal |
| `%d` | Decimal integer |
| `%i` | Integer in base 10 |
| `%u` | Unsigned decimal integer |
| `%x` | Hexadecimal integer (lowercase) |
| `%X` | Hexadecimal integer (uppercase) |
| `%%` | Literal percent sign |

---

## Author

Made by [Arthur-PRZ](https://github.com/Arthur-PRZ)
