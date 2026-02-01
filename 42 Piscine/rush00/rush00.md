
```
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   rush00.c                                           :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: epereira <epereira@student.42porto.com>    +#+  +:+       +#+        */
/*                                                +#+#+#+#+#+   +#+           */
/*   Created: 2026/01/31 14:29:28 by epereira          #+#    #+#             */
/*   Updated: 2026/02/01 14:24:51 by nda-roch         ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */

void	ft_putchar(char c);

char	ft_symbols(int posx, int posy, int x, int y)
{
	if ((posy == 1 && posx == 1) || (posy == 1 && posx == x)
		|| (posy == y && posx == 1) || (posy == y && posx == x))
	{
		return ('o');
	}
	if (posy == 1 || posy == y)
	{
		return ('-');
	}
	if (posx == 1 || posx == x)
	{
		return ('|');
	}
	return (' ');
}

void	ft_print(int x, int y)
{
	int	posx;
	int	posy;

	posy = 1;
	while (posy <= y)
	{
		posx = 1;
		while (posx <= x)
		{
			ft_putchar(ft_symbols(posx, posy, x, y));
			posx++;
		}
		ft_putchar('\n');
		posy++;
	}
}

void	rush(int x, int y)
{
	ft_print(x, y);
}
```