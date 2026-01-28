![[42 Piscine/shell00 (UNCOMPLETE)/Pasted image 20260127123646.png]]

Once you’ve achieved the previous steps, execute the following command to create
the file to be submitted:

 `tar -cf testShell00.tar testShell00`


create file testShell00


`touch testShell00`

## change permissions

`chmod`

# permissions:

- read (r) = 4 (em hex)
- write (w) = 2
- execute (x) = 1
dps e so somar

777 = all perms

# classes:

- user (u)
- group (g)
- other (o)

## format

-xxx(user)xxx(group)xxx(other)

## so, testShell00, has to have these permissions


-r--r-xr-x 

- **==r**--== **==r**-**x==** **==r**-**x==** 

`chmod u+r testShell00`
`chmod g+r testShell00`
`chmod g+x testShell00`
`chmod o+x testShell00`

added read perms to user, read and execute to group, execute to other

## change to 40 bytes

`truncate *file* -s 40`

Shrink or extend the size of each FILE to the specified size

-s, --size=SIZE
              set or adjust the file size by SIZE bytes
          

## change date

**–t** time

specifies a particular time using this format: `[[[[cc]yy]mm]dd]hhmm [.ss]`

where:

- cc is the first two digits of the year (optional)
- yy is the last two digits of the year (optional)
- mm is the number of the month (01—12) (optional)
- dd is the day of the month (optional)
- hh is the hour in 24-hour format (required)
- mm is the minutes (required)
- ss is the seconds (optional)

`touch -t 9406012342 testShell00`

`-t` = change time

94 (1994)

06 june

01 day

23:42 time


## create file to submit

> `tar -cf testShell00.tar testShell00`

create zip file
-c create
-f file
