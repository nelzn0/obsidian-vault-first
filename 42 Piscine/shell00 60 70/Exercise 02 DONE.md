same thing, but with 2 folders, 4 files, and one symlink

![[Pasted image 20260127143955.png]]

`mkdir test0`

`touch test1`

etc.

``
`ln -s test0 test6`

ln -s = create a **symlink**

`touch -h -t 9706012220 test6`

`-h` =  to not follow the link


## file to be submited

`tar -cf exo2.tar` 