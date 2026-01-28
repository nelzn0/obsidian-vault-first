Turn-in directory: ex01/
Files to turn in: `print_groups.sh`
Allowed functions: None

Write a command line that displays the list of groups the user (defined in the
environment variable FT_USER) belongs to.

• The output should be comma-separated, without spaces. yaa 

• Examples: a 

◦ for FT_USER=bocal:

![[42 Piscine/shell01/Pasted image 20260127115149.png]]

◦ for FT_USER=daemon:

![[42 Piscine/shell01/Pasted image 20260127115215.png]]

man id

```
id -Gn | tr ' ' ',' | cat -e
```



`id` = Print user and group information

`-G` = print group IDs

`-n` = group name

g + n = print a group name

id -gn {user}
 
`tr` = basically transform/replace characters in text

replace all spaces ' ' with a comma ','

`cat -e` to display all breaks as $

CORRECT ANSWER

`id -Gn $FT_USER | tr ' ' ',' | cat -`

Faltava me o $FT_USER



gemini:

I see exactly what's happening. In the world of automated grading (like the Moulinette used in 42 or similar bootcamps), the `cat -e` command is a classic "gotcha."

The exercise asks you to **display** the groups. The example shows the `$` at the end because it’s simulating what you see in a terminal when there is **no newline** at the end of the output.

### The Problem

When you use `cat -e`, you are telling the computer to actually **print** a literal `$` character. The grading script is expecting the list of groups, but it’s receiving a list of groups with a dollar sign typed on the end.

### The Fix

You need to replace `cat -e` with a command that removes the trailing newline that `id` naturally produces. The most common way to do this in shell exercises is using `tr -d '\n'`.

Try this instead:

Bash

```
id -Gn $FT_USER | tr ' ' ',' | tr -d '\n'
```

---

### Why this works:

1. **`id -Gn $FT_USER`**: Gets the groups.
    
2. **`tr ' ' ','`**: Swaps spaces for commas.
    
3. **`tr -d '\n'`**: Deletes the newline character. This "glues" your prompt to the end of the output, which matches the example `daemon,bin$>` (where `$>` is the next prompt).
    

### Important Check

Make sure your `print_groups.sh` file:

- Contains only that line.
    
- Has **no extra spaces** or empty lines at the end of the file.
    
- Is executable (`chmod +x print_groups.sh`).