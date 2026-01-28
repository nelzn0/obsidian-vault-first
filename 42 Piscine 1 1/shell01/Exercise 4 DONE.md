Turn-in directory: ex04/
Files to turn in: MAC.sh
Allowed functions: None

• Write a command line that displays your machine’s MAC addresses, with each
address followed by a line break.

man ifconfig

`ifconfig -a | grep ether | awk '{print $2}'`

ifconfig -a = display all interfaces

grep = basically a find command, finding every line that has ether

`ifconfig -a | grep ether`

ether 8e:fa:29:ab:35:97  txqueuelen 0  (Ethernet)
ether 00:be:43:91:1d:f4  txqueuelen 1000  (Ethernet)
ether 52:54:00:0c:32:07  txqueuelen 1000  (Ethernet)
ether c8:cb:9e:34:90:4f  txqueuelen 1000  (Ethernet)

now we need to display only the mac address

it at the second column

so, 

`ifconfig -a | grep ether | awk '{print $2}'`

`8e:fa:29:ab:35:97`
`00:be:43:91:1d:f4`
`52:54:00:0c:32:07`
`c8:cb:9e:34:90:4f`

awk '{print $2}' will only print the strings at the second column