Turn-in directory: ex06/
Files to turn in: skip.sh
Allowed functions: None

• Write a command line that executes `ls -l` but displays only every second line,
starting from the first line.

• Example output:

![[42 Piscine/shell01/Pasted image 20260127115809.png]]

`ls -l | awk 'NR%2==1'`

awk = find

NR = number of records

% = the rest of the division

%2 = every second record

== = the difference

==1 = verifies if the rest is 1, odd

==1 = starting from the first line


https://www.reddit.com/r/commandline/comments/1phfe0/how_would_i_read_every_nth_line_starting_from_nth/
