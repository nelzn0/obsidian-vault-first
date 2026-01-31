Turn-in directory: ex03/
Files to turn in: ft_div_mod.c
Allowed functions: None

• Create a function ft_div_mod with the following prototype:

![[Pasted image 20260129141325.png]]

`void ft_div_mod(int a, int b, int *div, int *mod);`

• This function divides ‘a’ by ‘b’ and stores the result in the integer pointed to by ‘div’. It also stores the remainder of the division of ‘a’ by ‘b’ in the integer pointed to by ‘mod’.

## resolution

`//#include <stdio.h>`

`void    ft_div_mod(int a, int b, int *div, int *mod)`
`{`
        `*div = (a / b);`
        `*mod = (a % b);`
`}`

`//int   main(void)`
`//{`
`//      int a = 4;`
`//      int b = 7;`
`//      int div;`
`//      int mod;`
`//      ft_div_mod(a, b, &div, &mod);`   
`//      printf("The division of each number is: %d \n", div);`
`//      printf("The rest of the division of each number is: %d \n", mod);`
`//      return (0);`
