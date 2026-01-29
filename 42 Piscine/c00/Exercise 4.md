Turn-in directory: ex04/
Files to turn in: ft_is_negative.c
Allowed functions: write

• Create a function that displays ’N’ or ’P’ depending on the sign of the integer passed as a parameter.

	◦ If n is negative, display ’N’.

	◦ If n is positive or zero, display ’P’.

• The function should be prototyped as follows:

![[Pasted image 20260128192558.png]]

## Solution

```
#include <unistd.h>

void ft_is_negative(int n)
{
        char c;
        {
                if (n <= -1)
                {
                        c = 'N';
                        write(1, &c, 1);
                }
                else
                {
                        c = 'P';
                        write(1, &c, 1);
                }
        }
}
```


first exercise I done completely from scratch with no help, however, I required perplexity to check because I got stuck on one part for using c& instead of &c.... LOL

todo cego

## to test

`int main(void)`
`{`
        `ft_is_negative(-3);`
        `return (0);`
`}`


or Positive

`int main(void)`
`{`
        `ft_is_negative(3);`
        `return (0);`
`}`
