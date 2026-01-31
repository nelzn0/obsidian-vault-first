Turn-in directory: ex06/
Files to turn in: ft_strlen.c
Allowed functions: None

• Create a function that counts and returns the number of characters in a string.

• The function should be prototyped as follows:

![[Pasted image 20260129141617.png]]

`int ft_strlen(char *str);`

## resolution


`#include <stdio.h>`

`int     ft_strlen(char *str)`
`{`
        `int i;`

        `i = 0;`

        `while (str[i] != '\0')`
        `{`
                `i++;`
        `}`

        `return i;`

`}`

`int main(void)`
`{`
        `char *c = "Hi";`
        `int count;`

        `count = ft_strlen(c);`

        `printf("the number of characters in this string is: %d ", count);`

        `return 0;`

`}`

ill use the index in the number of chars in string
to only count the number of strings,

and then i return the index value

to test

in main ill create a char variable with a pointer with a value

then a int variable for the count

and then ill assign the count value with my function that counts the index

then ill print it