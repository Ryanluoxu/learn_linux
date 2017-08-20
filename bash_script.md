# bash script
## c1 intro
- `755` - give execute permission: `chmod 755 filename`
- `./` - execute: `./filename`
- `#!/bin/bash` : use bash

## c2 variable
- `$1` `$2` - 1st, 2nd command line arguments
- `variable=value`
- `" "` - allow variable substitution
- `' '` - not allow
- `var=$(command)` - save the output of a command
- `export var` - make `var` available to child processes

## c3 input
- `read -p 'username: ' username`
- `read -sp 'password: ' password`
- `cut -d' ' -f 2,3`    
	- use ` ` as delimiter  
	- keep 2nd and 3th fields
- `/dev/stdin` - a file to get the STDIN
- `cat data.txt | ./result.txt`  
	- `data.txt` is the input of `result.txt`
	- and execute `result.txt` 

## c4 arithmetic
- `let` - make a variable = expression
- `expr` - print out the result of expression
- `$((expression))` - return the result of the expression
- `$(#var)` - return the length if the variable

## c5 if
### basic:  

```
if[<some test>]
then
	<command>
fi
```
example:

```
if [ $1 -gt 100]
then
	echo it is a large number
	
	if (( $1 % 2 == 0 ))
	then
		echo and it is also an even number
	fi

fi
```

- `\'` - '
- `date` - give current date time

### test command
- `!` - not
- `-n str` - the length of str is > 0
- `-z str` - the length of str is 0
- `str1 = str2`
- `int1 -eq int2` - int1 is numerically = int2
- `-gt` - greater than
- `-lt` - less than
- `-d file` - file exists and is a dir
- `-e file` - file exists
- `-r file` - file exists and read permission is granted
- `-s file` - not empty
- `-w file` - write permission
- `-x file` - execute permission

```
test 001 = 1
echo $? #1

test -s notexistingfile
echo $? #1
```
 
### if else

```
if [ ... ]
then
	...
else
	...
fi
```

¯
