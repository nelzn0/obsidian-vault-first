Turn-in directory: ex08/
Files to turn in: ft_sort_int_tab.c
Allowed functions: None

• Create a function that sorts an array of integers in ascending order.

• The function takes two arguments: a pointer to an int and the number of elements in the array.

• The function should be prototyped as follows:

![[Pasted image 20260129141810.png]]

`void ft_sort_int_tab(int *tab, int size);`

## resolution

```
//#include <stdio.h>

void    ft_sort_int_tab(int *tab, int size)
{
        int     temp;
        int     i;
        int     end;
        int     sorted;

        sorted = 0;
        i = 0;
        end = size - 1;
        while (sorted == 0)
        {
                sorted = 1;
                i = 0;
                while (i < size - 1)
                {
                        if (tab[i] > tab[i + 1])
                        {
                                temp = tab[i];
                                tab[i] = tab[i + 1];
                                tab[i + 1] = temp;
                                sorted = 0;
                        }
                        i++;
                }
        }
}
int   main(void)
{
        int tab[] = {9, 8, 7, 6, 5, 4, 3, 2, 1};
      ft_sort_int_tab(tab, 9);
      int i = 0;
      while(i < 9)
      {       
      printf(" %d ", tab[i]);
      i++;
      }
      return (0);
}
```

end var is useless now, i've included it oops

added sorted var, 0 means its not sorted, 1 means it sorted

I started with sorted = 0 to assume its not sorted

then a loop, while the table isnt sorted (0)

assume that its already sorted

set the index back to the first position

then another loop, comparing the current position to the next, with a minus one in the size since the first position is always 0

with a increment for the index

inside this loop we have an if the current position is bigger than the next position, we swap it

we put the current position in the temp

the next position in the current position

and then we put the current position saved on temp in the next position








