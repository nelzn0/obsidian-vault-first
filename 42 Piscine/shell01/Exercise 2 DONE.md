Turn-in directory: ex02/
Files to turn in: `find_sh.sh`
Allowed functions: None

Write a command line that searches for all files ending with .sh in the current
directory and all subdirectories. a 

• The output should display only the file names without the .sh extension.

• Example output:

![[42 Piscine/shell01/Pasted image 20260127115314.png]]

`find . -name "*.sh"`

but now without .sh extension

https://man7.org/linux/man-pages/man1/find.1.html


`find . -name "*.sh" -exec basename {} .sh \;`

`-exec basename`

exec = executes a command

-exec = makes it possible to execute in find

basename = only show the filename

{} = path of the file

.sh = tells basename to remove .sh from the name

`find . -name "*.sh" -exec basename {} .sh \; 

cat -e to add $ in breaks

Tinha o `| cat -e` dentro do ficheiro a toa, e um espaco

