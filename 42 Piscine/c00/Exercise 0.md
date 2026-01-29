Turn-in directory: ex00/
Files to turn in: ft_putchar.c
Allowed functions: write

Write a function that displays the character passed as a parameter.

• The function should be prototyped as follows:

![[Pasted image 20260128175638.png]]

• To display the character, you must use the write function as follows:

![[Pasted image 20260128175700.png]]


## I guess I only need to do this?

`#include <unistd.h>`

`void ft_putchar(char c)`
	`{`	
		`write(1, &c, 1);`
	`}`

1 = is a file descriptor, 1 = standard output
&c - is the address of c, a pointer for the variable, so i can change it however i want
second 1 = write only 1 byte


## And to test it

`int main (void)`
        `{`
                `ft_putchar('A');`
                `ft_putchar('\n');`
                `return (0);`
        `}`

paremeter A so I can print A, and another one with a new line

always return 0 to end the program
