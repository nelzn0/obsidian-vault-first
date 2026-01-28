Turn-in directory: ex03/
Files to turn in: count_files.sh
Allowed functions: None

• Write a command line that counts and displays the total number of regular files
and directories in the current directory and all its subdirectories. a

• The count should include "." (the starting directory).

• Example output:

![[42 Piscine/shell01/Pasted image 20260127115418.png]]

`ls -1 | wc -l'

`ls` = list files

`-1` = list 1 line at a time

`wc` = word count)

`-l` = count number of lines