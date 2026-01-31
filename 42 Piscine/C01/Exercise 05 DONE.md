Turn-in directory: ex05/
Files to turn in: ft_putstr.c
Allowed functions: write

• Create a function that displays a string of characters on the standard output.

• The function should be prototyped as follows:

![[Pasted image 20260129141516.png]]
`void ft_putstr(char *str);`




## resolution

`#include <unistd.h>`

`void    ft_putstr(char *str)`
`{`
        `int i;`

        `i = 0;`

        `while (str[i] != '\0')`
        `{`
                `write(1, &str[i], 1);`
                `i++;`
        `}`

`}`
                
`int main(void)`
`{`
        `ft_putstr("Hello");`
        `return 0;`
`}`

string is a sequence of char in memory, one after another

it stops with a specific character '\0' (null), the end of a string

using a int var named "i", my index, with 0 meaning its starting at his first character

while the character of the string isnt /0 (the end)

write a single character of the string, byte by byte

&str[i] = the address of the current character

i + 1 for the next character







## one type of resolution (idk if its right)

#include <unistd.h>

`void    ft_putstr(char *str)`
`{`
        `while (*str)`
        `{`
                `write(1, str, 1);`
                `str++;`
        `}`

`}`

`int main(void)`
`{`
        `char test[] = "Testing";`
        `ft_putstr(test);`
        `return 0;`
`}`