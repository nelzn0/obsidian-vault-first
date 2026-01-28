In a file called clean write a single command that:
◦ Searches for all files in the current directory and its subdirectories that end
with ~ (tilde) or, start and end with # (hash).
◦ Displays the found files and deletes them.
• Only one command is allowed, no ’;’ or ’&&’ or other chaining tricks

man find

![[Pasted image 20260127110354.png]]

might be this

`find . -name "*~"`


getting there

`find . -name "*~" -delete`

successfully deleted a ~ file

agora tenho de meter todos os argumentos no name

`#* comeca com #`

`*# acaba com #`

`*~ acaba com ~`

got it, it with `-or` 

`find . -name "#*" -or -name "*~" -or -name "*#"`


`-delete` no fim nao deu, porem

`find . -name "#*" -delete -or -name "*~" -delete -or -name "*#" -delete`

assim ja da

mas tenho de display o que apaguei

imagino que seja com -print em cada

`find . -name "#*" -delete -print -or -name "*~" -delete -print -or -name "*#" -delete -print`

start and end maybe

`find . -name "#*#" -delete -print -or -name "*~" -delete -print'







