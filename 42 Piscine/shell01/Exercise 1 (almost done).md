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

`groups $FT_USER | tr ' ' ',' | cat -e`

`cat -e` to display all breaks as $

