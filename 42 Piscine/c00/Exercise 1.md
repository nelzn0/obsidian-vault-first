Turn-in directory: ex01/
Files to turn in: ft_print_alphabet.c
Allowed functions: write

• Create a function that displays the alphabet in lowercase, on a single line, in ascending order, starting from the letter ’a’.

• The function should be prototyped as follows:

![[Pasted image 20260128192300.png]]

## Solution

`#include <unistd.h>`

`void ft_print_alphabet(void)`
`{`
        `char letter;`
        `{`
                `letter = 'a';`

                `while (letter <= 'z')`
                `{`
                        `write(1, &letter, 1);`
                        `letter++;`
                `}`
        `}`
`}`

create a char variable letter

create a loop

while letter is less or equal than z then

write standard output, pointer for the var letter, 1 byte

counter letter (letter + 1)


## to test it

`int main (void)`
`{`
        `ft_print_alphabet();`
        `return (0);`
`}`

just call function