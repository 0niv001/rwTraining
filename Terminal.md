---
sticker: lucide//terminal-square
---
Unix: Small modular programs that can perform complex tasks when put together. 
Kernel is to OS what engine is to a car. Key, but not all that is. 
*Shell*: Interface that translates commands to OS. 

**Basics:**
- Options can be combined together into single dash (-)
- Double dash for verbose option
- Some options have parameters
```command -options argument```

**Man pages / Help**
- Space / f to go down 1 page at the time
- b to go back
- h for other commands list
- search section using -k option. 
```BASH
/ or ? pattern -> search forward/backwards e.g. /-w

type -> what type of command something is e.g alias 
which -> where command is located
help -> use with commands in built in shell, no shortcuts. 
```

**Navigation**
- Home ~ shorthand
- Root /  shorthand. 
```Bash
pwd -> where am I?
ls ->  -l (more info), -a (hidden files), -R
```

**Creating files and folders**
```Bash
touch [path] -> create multiple by spacing argument
mkdir -> -p to create folder structure with parents
file -> file type
```

> [!Naming conventions]
> No punctuation, slashes and quotes
> No spaces
> Use dash and underline 

**Nano / Pico** 
- nano FILE -> even if it does not exist

**Deleting, Copying & Moving**
- Make sure directories exists when trying to move it to another one. 
- Can use .. to move files up one. 
- Can rename and move all at once. 
``` Bash
rm -> -d (directory) | -r (everything specified)
mv FILE/FOLDER LOCATION -> can use absolute and relative paths
mv <current name> <new name>
cp <source> <destination> <name>
```

**Shortcuts**
```
ctrl + l -> to clear entire screen
ctrl + a -> move to beginning of line
ctrl + e -> move to end of line
ctrl + f/b -> move cursor one char at the time, same as arrows
opt + arrows -> move one word at the time
ctrl + t -> swaps characters
opt + t -> swaps words 
ctrl + k -> kill from cursor to end of line 
ctrl + u -> from cursor to beginning of the line 
opt + d -> deletes the word. 
ctrl + y -> take back what you deleted
history -> look at history !number -> run command from history
ctrl + r -> search through history
!! -> previous command
```

**Working with files**
- less works in the same way as the man pages with the same shortcuts. 
- head and tail work in the same way like in Python. 
- None of these change the output of a file. 
- Field sort -> -k\[number] to specify which field to sort. 
```BASH
cat FILE -> read file and print it out. 
cat FILE1 FILE2 -> join content then output. 
less FILE -> show content of file, 1 page at the time. (for big files)
tac -> reverse of cat
head / tail [-NUMBER]
wc -> word count [-l] lines
sort -> alphaB line by line. / -r reverse / -n for numbers / -u unique
```

**Redirection**
- STDOUT -> output command to a file / server or printer. 
	- Can use it to quickly create a file. e.g.
- STD ERR -> output errors to a different place other than terminal. 
- STDIN -> Input can come from files and other commands. 
- Can do STDIN & STDOUT at the same time. use &>
```Bash
STDOUT
<cmd> > <file/loc>  Redirect output / Overwrites anything if existing. 
<cmd> >> <file> Append output instead of overwrite
echo "text" > <file> to quickly create file. 

STDIN
<cmd> < <file> passing something as input. 

STDERR
2> or 2>> 
```

**Piping**
```BASH
ls -l | less
tr -> replace input with certain output, can use ranges
cmd | tee FILE | cmd2 -> takes input and cps to stout and file
```

**Expansion**
- Multiple stars can also be used to expand wildcard. 
- Can have multiple and nested brace expansions. 
```BASH
ls *.html / cat blue*-> multiple files & paths, anything with blue in name
ls pic?.png / pic.?? -> any single character, exact numbers. 
[range] -> [0-9/ A-Z/ 123] or []* can negate range using [^]
~USER -> expands into other user directory. 
touch page{1,2,3 / 1...4}.txt -> create strings according to pattern
echo $((Expression)) to do maths.  
Single quote to suppress all substitution, double to keep some
today is $(date) or `date`-> substitues command, like with variables. 
```

**Finding things**
- Locate uses pre made DB, making it fast, can locate from anywhere you are
	- l {num} - limit , i ignore case ,  e check if files exist n DB
	- updatedb to update it 
	- -size ±\[number]k/m/g
- Find is much slower than locate
	- -type f or d / files and folders
	- -name "names" -> case sensitive and exact unless using iname
	- Searches from where you are
	- Can use patterns \"*[0-9]*"
	- -empty 
	- -and -or ! logical operators. 
```BASH
locate -> search for pattern that matches
find 
```

**Grep**
- Search within files. 
```BASH

```

**Permissions**
- Can have multiple users per session at the same time. 
- Owner can change permissions, as well as group owners. 
- rwx => Owner - Group - World 
```BASH
l-d rwxr- -> file,directory or symbolic link, read, write, execute, 

su -> switch user 
```

**Environment**
- Info stored during a shell session, in key value pairs. 
- Can get env variable using $ -> parameter expansion. 
- Built in variables are in all CAPS
```BASH
printenv -> view environment variables
$USER -> get USER env variable
```

**Scripting**
- Putting script in PATH variable allows the to be found anywhere
```BASH
#!/bin/bash -> shebang, tells the os what interpreter to use, then the path of the file

# to comment
```

**Cron**
- Schedule commands at regular intervals. 

```

```