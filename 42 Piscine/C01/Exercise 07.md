Turn-in directory: ex07/
Files to turn in: ft_rev_int_tab.c
Allowed functions: None

• Create a function that reverses a given array of integers (the first element becomes the last, and so on).

• The function takes two arguments: a pointer to an int and the number of elements in the array.

• The function should be prototyped as follows:

![[Pasted image 20260129141725.png]]

`void ft_rev_int_tab(int *tab, int size);`

## resolution

`//#include <stdio.h>`

`void    ft_rev_int_tab(int *tab, int size)`
`{`
        `int     temp;`
        `int     i;`
        `int     end;`

        `i = 0;`
        `end = size - 1;`
        `while (i < size / 2)`
        `{`
                `temp = tab[i];`
                `tab[i] = tab[end];`
                `tab[end] = temp;`
                `i++;`
                `end--;`
        `}`
`}`
`//int   main(void)`
`//{`
`//      int tab[] = {1, 2, 3, 4, 5, 6, 7, 8, 9};`
`//      ft_rev_int_tab(tab, 9);`
`//      int i = 0;`
`//      while(i < 9)`
`//      {`       
`//      printf(" %d ", tab[i]);`
`//      i++;`
`//      }`
`//      return (0);`
`//}`

in the function i created 3 int vars

a temporary var
the index var
and the end (of my index) var

always set the index to the first position (0);
I set the end var, size minus one (since the first position is
usually not 1, but 0)

and then a loop
