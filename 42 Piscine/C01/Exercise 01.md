Turn-in directory: ex01/
Files to turn in: ft_ultimate_ft.c
Allowed functions: None

• Create a function that takes a pointer to a pointer to a pointer to a pointer to a pointer to a pointer to a pointer to a pointer to a pointer to an int as a parameter and sets the value of that int to “42”.

• The function should be prototyped as follows:

![[Pasted image 20260129141009.png]]

`void ft_ultimate_ft(int *********nbr);`

## resolution

`#include <stdio.h>`

`void    ft_ultimate_ft(int *********nbr)`
`{`
        `*********nbr = 42;`
`}`

`int     main(void)`
`{`
        `int n = 5;`

        `int *p1 = &n;`
        `int **p2 = &p1;`
        `int ***p3 = &p2;`
        `int ****p4 = &p3;`
        `int *****p5 = &p4;`
        `int ******p6 = &p5;`
        `int *******p7 = &p6;`
        `int ********p8 = &p7;`
        `int *********p9 = &p8;`

        `printf("number before: %d \n", n);`

        `ft_ultimate_ft(p9);`

        `printf("number after: %d \n", n);`

        `return (0);`
`}`

Basically I had to made multiple pointers lol

my first value, n, would be 5

then i would it to the first pointer

then i would point the first pointer to the second

then the second to the third

then the third to the forth

etc

until the 9th pointer has the value of everyyy pointer

then I will call the function with the value of the 9th pointer

and print it! done

