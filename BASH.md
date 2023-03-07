# DAY 1: BASH
 
### Bash information:
	```
	-Bash stands for Bourne Again.
	-Unix shell to interact with operating system.
	-Bash widely used on linux
	-command line environment for excuting scripting tasks.
	-supports job control, command-line editing, and command history
	-writenn similar
    
#### Linux Command and Switches:
   	 
    	```
    	history:
    	!<his number> to reference command
    	history | egrep <command> <---------searcheshistory when used command
    	```
   	 
  **reverse i search in bash ctrl + r  and type char**
   	 
   	 
   	 
   **ctrl + a takes you to begining of command**
   
   
   
### Getting help man:
   ```
   - man (command) | egrep "pattern"
   -man bash bash man page
   -man find opens man page for finf command
   -G end of page
   -g start of man page
   -/pattern search forward for (N-th) matching line
   -&pattern Seach backward for (N-th) matching line
   n or shift+n moves between search results
   b to go up
   q	Quit man
   
   ```
   
### Online resources:
   
 	 
 	 
   Additional Links for Research:
https://linux.die.net/man - Online Man Pages. (Search wget as example)

https://serverfault.com - Question and Answer site. May help you get command suggestions if you know what you’re trying to do. (Search "linux history"  	or "user input" as examples)

https://ss64.com/bash - Breaks down options and has examples at the bottom usually. (Show "apt-get" as example)

https://stackoverflow.com - Good resource when using Google for specific syntax questions. Utilize carefully because an answer you find may not answer  	YOUR question. (Search "grep" as example)

https://tldp.org/LDP/abs/html/index.html - In depth explanations and good examples. (Show "Special Characters" and "Loops" as examples)

http://bit.ly/USACYSscripting - Google Drive which includes helpful examples. (Show AWK)

https://www.gnu.org/software/bash/manual/ - For advanced students who want to know how BASH works in the background.

https://linuxize.com/post/bash-if-else-statement/ - Good examples of if/else statements.

https://google.com - Make Google work FOR you by asking the right questions. (Google "How to take user input with Bash" as example) (edited)

    
### Order of Evalution: The order the computer finds a command
	```
	1.Redirection <- file need to create file so it happens first
      	> output writes to new file
      	>> append end of file
      	stad in 	stad out  	stad err
      	STDIN   	STDOUT     	STDERR
      	keyboard	monitor    	on how code works
                	|   bof on monitor -------------->
      	send STDERR to dev null if dont want to troubleshoot   
     	 
     	 
	2.Alias  
    
	alias cat='echo "Nothing to see here"' is example of using alias command unalias to redo it which to find path of command
    	use type tells type of command if alias type -a goes further alias if first the nfunction then binary
   	 
    	unalias <alias>
    	unset <function> <- function
    	now the uinset function is a bin
    
	3.Parameter expansion, comand substitution, arthimetic expansion, and quote removal.
    	touch creates file
    	touch <file> or touch file file file
        	brace expansion uses {}
       	 
 	**touch file{1..100}**
 	**rm file*** <-- globbing**
  	rm * removes everything in directory
 	 
 	 
	**4.shell function**
    
	5.built -in commands
    	built in commmand dont have man pages use help <command>
   	 
	6.hash tables
    	cache
   	 
	7.pth variable
    	echo $PATH is the  seperated by colon helps speed up computers
    	hash command shows cache for command hash table
    	sudo rm /bin/<command>
    	if run that command it doesnt exist
    	hash -r clears hash table
    	hash = no hash
   	 
	8.error (eg command not found)
    	if this happens command not found
   
   
    
    
### Command chaining operators: <_--- part of number 3
    	```
    	sleep 5 & <-- sleep for five  secrond in the background
    	; <----
    	command;command; runs sequnce if works in session
     	ls;cat file STDIO one command STDERR other
     	can use this to get output of multiple command
    	 
  &   --Sends process to background (so we can run multiple process parallel) \
  ;   --Run multiple commands in one run, sequentially.\
  \  --To type larger command in multiple lines\
  &&  --Logical AND operator <-- run if first runs properly FIRST HAS TO WORK\
  ||  --Logical OR operator <--- cmd1 || cmd2 || cmd3 cmd2 will only run will cmd1 fails \
  !   --NOT operator\
  |   -- PIPE operator\
  {}  --Command combination operator.\
	[ -f 99.txt ] || { echo " does not exist"; touch 99.txt; }\
  ()  --Precedence operator\



### File System and Manipulation:
   
	Absolute   /root is admin / top of file system
	relative   if cd .. cd //
	pwd shows where your at
	cd /home cd/home/student $HOME
	cd / root of file system
	cd ~ back to home
	cd $HOME home directory
	./ relative file path reference
	cd byitself takes you home
	cd - toggle between last to locations
    	```
      	- Absolute, Home, and Relative File reference
     	 
        	home dir  	~/ or $HOME
        	ab path   	/etc/passwd
        	relv path 	./ or ..
       	 
        	filesystem cmds
        	touch   	touch -t [[CC]YY]MMDDhhmm[.ss]
        	mkdir   	mkdir -p
        	rm      	rm -rf
        	rmdir   	rmdir -p
        	ls      	ls
        	cd      	cd -
       	 
        	links
       	 
        	sysmbolic link	A shoprtcut or pointer
        	hard link 	Persistent, cannot cross file systems
       	 
       	 
        	.<file> hidden file
        	ls -a to look at hidden files
         	 
      	```
    	curl equilivant of cat
     	 
     	 
**curl cht.sh/grep** <--- bettecurlr man page for grep can be used on any command SHOW EXAMPLES

**explianshell.com** explains the command   



###  Processes and Memory:
	Process Hierarchy
  	kernel
    	Init - 01
        	BASH
           	ps
      	process snapshot
        	- ps -elf
      	terminating:
          	-kill	kill -9 1234
          	-killall  killall firefox
         	 
         	 
         	 
### Cat More || Less
    	cat(1) - conatenate files and print on the standard outut" -n line numbers
        	head top 10 lines by default
        	tail last 10 lines default
        	less parse easier
        	more
          	 
   	 
### Finding Files and Dirs:
   
  	Find(1) - search for files in a directory hierarchy" does recrusion by default
  	-locate 	looks for certain file */<file>*
  	-whereis	like which but man page
  	-which  	file path
  	-find  	 
  	whatis  	summary of what command does
  	what do we use find for?
      	Does it parse through the content or just files
      	Is it limited to just fikenames or what can it search by?
     	 
     	 
            	find -iname ".conf" denotes case- insensitive file anything ending .conf
   	 
        	find [LOCATION] [OPTIONS]
              	find /etc -iname "*.conf" 2>/dev/null
              	find /etc -iname "*.conf"  > /dev/null <-- displays errors to screen
             	 
             	find -maxdepth <dirs deep> only a certain directory deep
             	file -type   f 	only displays files
             	find -mtime 2	modified 2 days ago
            	 
  **-mmim**           	<-- find out difference of mmim and mtime
		 
### exec option:

             find $HOME/1123/?.txt -type f -exec cp "{}" $HOME/CUT \;
           	 
             -exec based on what it founf execute aginst eahc item in my output
            	 
            	 
             ls -l PATH/TO/DIRECTORY grep[OPTIONS]"pattern" {} ls {} grep pattern {}
            	 
            	 

# DAY TWO

### Overview
	Conditionals
		-e file exists?
		-f file exists and is a regular file?
		-d file exists and is a directory
		== strings, is equal to strings
		-eq numbers, is equal to 
		!= strings, is NOT equal to
	Command Substitution
	Commands
		alias - views all alias
			alias vim='nano' - creates an alias for vim to be the command nano
			unalias vim - resets the vim alias to the vim command
		sort - sort content according to the position on the ASCII table
			sort -n sorts contents numerically
			sort -u sorts contents uniquely
			sort -r sort content reversed
		uniq - select content uniquely, must already be sorted first
			uniq -c slect content uniquely a count reading
			uniq -u display on the unique lines(lines without duplicates)
			uniq -d display only the duplicate lines (opposite of -u)
		awk - pattern searching and process language
			syntax - awk [options] 'selection_criteria {action }' input-file > output-file
			awk -F: '{print $1}' - displays 1st field delimited by a ":"
			awk '{print $2}' - displays 2nd field; delimited automatically by white space.	
				$1..9 or $nf - this will always print the last one, no matter what it is
		sed - stream editor for filtering and transforming text
			sed 's/abc/123/' - replace first occurence of abc in every line with 123
			sed 's/abc/123/g' - replace every occurence of abc in every line with 123
			sed '/sus/d' - delete the sus lines. output everything else
			sed -i '<expression>' file.txt - "sed inplace" to make changes permanent in file.txt
		Activities 6-10

### Demo Time

##### Alias
Examples of the command alias
```
alias hello='echo "Hello, is it me you're looking for"'
unalias hello
\(alias) - this negates the alias set and uses the actual command
```

##### Sort and uniq
```
sort (file) | uniq -c | sort -r - this sorts the file, gets a count of every item, and then sorts again but from most used to least used
sort -t',' -k2nr (file) | cut -d, -f1
```

##### Awk

```
egrep "root" /etc/passwd | awk -F: '{print $1,$3,$4}'

egrep "root" /etc/passwd | awk -F: '{print $1}'

date | awk '{print $2,$3,$NF}'

egrep "/bin/false|bin/bash" /etc/passwd | awk -F: '($7="/bin/bash"){print $0}'

echo "Python is better than Bash" | awk '{$1=" Bash";$5="Python";print}' - this swaps python and bash

echo "Python is better than Bash" | awl '{$1="Marines";$2="are";$5="Soliders";print}' - this replaces the word at each spot with the new ones mentioned

SUBJECT=Leaders
VERB=inspire
OBJECT=people
echo $SUBJECT - relays back what it is

echo "Managers manage equipment" | awk -v ss=$SUBJECT -v vv=$VERB -v oo=$OBJECT '{$1=ss;$2=vv;$3=oo;print}'
You made variables above, and then using awk, replaced the echo command we set with the variables above
```

##### Sed

```
sed 's/FINDPATTERN/REPLACEPATTERN/' - the g replaces EVERY occurence

erep "student|root" /etc/passwd | sed 's/student/instructor/g'

egrep "student|root" /etc/passwd | sed 's/\/bin\/bash/\/bin/\/better/g' - if the thing you are trying to replace has "/" you need to escape "\" them out

egrep "student|root" /etc/passwd | sed 's+/bin/bash+/bin/sus+g' - does the same thing as above, just easier to not mess up

egrep "student|root" /etc/passwd | sed -e 's+/bin/bash+/bin/sus+g' -e 's*student*Hackerman*g'
you can replace multiple instances in one line, just need to use -e option


egrep "student|root" /etc/passwd | sed '/root/d'
```

# Day three

### Parameter vs Variable

	In a bash context a parameter is an entity that stores values.
	Furthermore, a parameter can be a 
		name(variable)
		number(positional parameter)
		special character(special parameter)
	Therefore, a variable is a parameter denoted by a name
		see "man bash"
	
	Variables
		Variables are parameters set with a name (identifier) on the left of an equal sign and a value (or 		   nothing) on the right side. Variables are user defined. (There cannot be any spaces on either side)
	
`	**Logical Paramters**
		$? - This parameter represents the exit status of the last command that executed. The 0 code 			represents success and 1 represents failure.
		
		$# - This parameter represents the number of arguments passed to the shell script
		
		$$ - This parameter gives the PID of the current shell
		
		$- - this parameter represents the current flags set in your shell .himBH are the flags in bash shell
		
		**Flags**
			H - histexpand
			M - monitor
			h - hashall
			B - braceexpand
			i - interactive


### Functions
```
	Allow breaking of code into more manageable blocks
	Series of commands executed as if a single command
	Can contain cariables, loops, accept parameters, and return a value
	Declare functions first, then call it
	There are few different formats/styles for laying out a function
```
**Demo: function.sh**
```
#!/bin/bash
   
   #--Function declaration
   
   function focus() {
       echo '"Your focus determines your reality." - Qui-Gon Jin'
   }
   
   function odds() {
      echo '"Never tell me the odds." -Han Solo'
  }
  
  hello() {
      echo '"Hello there!" -Obi-Wan Kenobi'
  }
  #--Invoke the functions
  focus
  odds
  hello
```

### Variable substitution

	Ultimately, its just replacing a variable with its value.


**DEMO**
```
#!/bin/bash
  
  sub1 () {
      name="John"
      echo $name
  }
  
  sub2 () {
      #Variable subsitution within double quotes
      name="John"
      echo "My name is $name"
  }
  
  sub3 () {
      #variable substitution with single quotes
      name="John"
      echo 'My name is $name'
  }
  
  sub4 () {
      #Using curly braces to seperate variables surrounding text
      name="John"
      echo "My name is $namenny5"
      echo "My name is ${name}nny5"
  }
  
  sub5 () {
      #Use curly braces to substitute the value of a variable inside parameter expansion
      name="John"
      echo ${name:0:2}
  }
  
  ##--Invoke the functions
  #sub1
  #sub2
  #sub3
  #sub4
  sub5
```

# Day Four

### For loops

	The for loop iterates over a list of items and performs the given set of commands. The Bash for loop takes the following form: for item in [LIST] do [COMMANDS] done. 
	Psuedo-Code
		for item in [LIST]
		do
		[COMMANDS]
		done
	ie
```
#!/bin/bash

for i in {1..10}
do
	echo $i
done
```

The LIST can be a series of strings seperated by spaces, a range of numbers, output of a command, an array and so on. All loops are great for automating repetitive tasks!

### Break and Continue IF statements
	The break statement terminates the current loop and passes program control to the statement that follows the terminated statement. It is usually used to terminate the loop when a certain condition is met.
	if [[ <condition> ]];then
		break
	fi
	
	The continue statement exits the current iteration of a loop and passes program control to the next iteration of the loop
	if [[ <condition> ]];then
		continue
	fi

### While and Until loops
	The while loop is used to perform a given set of commands an unknown number of times as long as the given condition evaluates to true.

```
#!/bin/bash
counter=1
while [[ $counter -le 10 ]]
do
	echo $counter
	((counter++))
done
echo "All done!"
```
	The until loop is used to execute a given set of commands as long as the given condition evaluates to false.

```
#!/bin/bash
counter=1
until [[ counter -gt 10 ]]
do
	echo $counter
	((counter++))
done
echo "All done!"
	echo
```

### Demo time

```
listo () {
     for NAME in Yager Lindner Alley
     do
         echo $NAME
     done
 }
 
 #listo
 
 listo2 () {
     names='Tenbusch Mills Regan'
     for NAME in $names
     do
         echo $NAME
     done
 }
 
 #listo2
 
 range () {
     for value in {1..5}
     do
         echo $value
     done
     echo "All done!"
 }
 
 #range
  
 rocket () {
     for value in {10..1}
     do
         echo $value
         sleep 1
     done
     echo "Team Rocket blasts off again!"
 }
 
 #rocket
 
 countloop () {
     for ((x=0;x<=5;x++))
     do
         echo "\$x is equal to $x"
     done
 }
 
 #countloop
 
 countloop2 () {
     start=1
     end=5
     for ((i=start;i<=end;i++))
     do
         echo $i
     done
 }
 
 #countloop2
 
 lightyear () {
     i=0
     for (( ; ; ))
     do
         echo "iteration: $i - To Infinity and Beyond!"
         ((i++))
         if [[ $i -gt 9000 ]];then
            echo "It's over 9000!!!"
            break
        fi
    done
}

#lightyear

thanksdad () {
    for i in {1..10}
    do
        if [[ $i -eq 9 ]];then
            continue
        fi
        echo $i
        ((i++))
    done
    echo "Son: Dad don't"
    echo "Dad: Well, looks like seven eight nine...RIP nine"
    echo "Son: ::groans::"
}

#thanksdad

beepbeep () {
    jeep_owners=1
    while [[ $jeep_owners -gt 0 ]]
    do
        echo "How many Jeep owners does it take to change a lightbulb?"
        read -p "Enter your guess " guess

        if [[ $guess -eq 0 ]];then
            echo "None, they just buy a new Jeep instead."
            ((jeep_owners--))
        elif [[ $guess -lt 0 ]];then
            echo "Invalid guess. Try again."
        else
            echo "Sorry, thats not the right answer."
        fi
    done
    echo "Congratulations, all the Jeep owners have given up trying to change the lightbulb!"
}

#beepbeep

autobots () {
    counter=10
    until [[ $counter -eq 1 ]]
    do
        echo $counter
        ((counter--))
    done
    echo "'Til all are one -Autobots'"
}

autobots
```







# BASH CTFd Challenges and OpNotes

### Question one (Brace Expansion)

Activity: Using Brace-Expansion, create the following directories within the $HOME directory:

1123
1134
1145
1156

```
mkdir $HOME/11{23,34,45,56}
```
This makes 4 directories within the $HOME directory.

### Question one part two

Activity:

Use Brace-Expansion to create the following files within the $HOME/1123 directory. You may need to create the $HOME/1123 directory. Make the following files, but utilze Brace Expansion to make all nine files with one touch command.

```
touch $HOME/1123/{1..5}.txt $HOME/1123/{6..9}~.txt
```
This makes 5 files with the .txt and 4 files with the ~.txt

### Question one part three

Activity:

Using the find command, list all files in $HOME/1123 that end in .txt.

```
find $HOME/1123/*".txt" -type f
```
This command finds only .txt FILES within the $HOME/1123 directory

### Question one part four

*Challenge Activity:
List all files in $HOME/1123 that end in .txt. Omit the files containing a tilde (~) character.*
##### Solution one:
```
find $HOME/1123/*".txt" | grep -v "~"
```
##### Solution two:
```
find $HOME/1123 -iname "*.txt" ! -iname "*~*"
```
##### Solution three:
```
find $HOME/1123 -name "*[^~].txt"
```
These commands finds all files with the .txt extension within the $HOME/1123 directory but doesnt display the ones with the "~" character

### Question two

Activity:

Copy all files in the $HOME/1123 directory, that end in ".txt", and omit files containing a tilde "~" character, to directory $HOME/CUT.

```
find $HOME/1123 -iname "*.txt" ! -iname "*~*" -exec cp {} $HOME/CUT \;
```
This command finds all files with .txt excluding any "~" and copies the contents into the $HOME/CUT directory

### Question three

Activity:

Using ONLY the find command, find all empty files/directories in directory /var and print out ONLY the filename (not absolute path), and the inode number, separated by newlines.

```
find /var -empty -printf "%i %f\n"
```
This command searches withing the /var directory for empty files and directories (-empty) and prints (-printf) only the inode number (%i) and ONLY the filename not absolute path (%f) seperated with a new line (\n)

### Question four

Activity:

Using ONLY the find command, find all files on the system with inode 4026532575 and print only the filename to the screen, not the absolute path to the file, separating each filename with a newline. Ensure unneeded output is not visible.

```
find / -inum "40265352575" -printf "%f\n" 2> /dev/null
```
This command searches the /var directory for files in the system with a specific inode number (-inum) and printing the file name only not absolute path (%f) seperating each filename with a newline (\n)

### Question five

Activity:

Using only the ls -l and cut Commands, write a BASH script that shows all filenames with extensions ie: 1.txt, etc., but no directories, in $HOME/CUT.
Write those to a text file called names in $HOME/CUT directory.
Omit the names filename from your output.

```
ls -l $HOME/CUT |cut -d. -f1- -s | cut -d: -f2 | cut -d' ' -f2 > $HOME/CUT/names
```
This command cuts

# Section two of activities

### Question six

Activity:

Write a basic bash script that greps ONLY the IP addresses in the text file provided (named StoryHiddenIPs in the current directory); sort them uniquely by number of times they appear.

```
egrep -o "(\b25[0-5]|\b2[0-4][0-9]|\b[01]?[0-9][0-9]?)(\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)){3}" StoryHiddenIPs | sort | uniq -c | sort -r
```
This command only grabs the ip address (egrep -o) in the StoryHiddenIPs file and then sorts them uniquely by the number of times they appear, so you must first sort then uniq them, then sort by the highest number

### Question seven

Activity:

Using ONLY the awk command, write a BASH one-liner script that extracts ONLY the names of all the system and user accounts that are not UIDs 0-3.
Only display those that use /bin/bash as their default shell.
The input file is named $HOME/passwd and is located in the current directory.
Output the results to a file called $HOME/SED/names.txt

```
awk -F: '($3>3 && $NF == "/bin/bash") {print $1}' $HOME/passwd > $HOME/SED/names.txt
```
This command looks at the entire $HOME/passwd directory and every UID thats not 0-3 ($3>3) and thats using /bin/bash ($NF == "/bin/bash") and printing ONLY the name ($print $1) and then outputting the results to the $HOME/SED/names.txt file

### Question eight

Activity:

Find all dmesg kernel messages that contain CPU or BIOS (uppercase) in the string, but not usable or reserved (case-insensitive)
Print only the msg itself, omitting the bracketed numerical expressions ie: [1.132775]

```
dmesg | grep 'CPU\|BIOS' | sed '/usable/d' | sed '/reserved/d' | cut -d] -f2-
```
This command searches the dmesg logs, greps for CPU and BIOS only (case sensitive) then removing any lines that contain usable or reserved using sed. Then cutting on the first delimiter that all options have so "]" in this case then print the second field and everything beyond

### Question nine

*Activity:
Write a Bash script using "Command Substitution" to replace all passwords, using openssl, from the file $HOME/PASS/shadow.txt with the MD5 encrypted password: Password1234, with salt: bad4u
Output of this command should go to the screen/standard output.
You are not limited to a particular command, however you must use openssl. Type man openssl passwd for more information.*

```
var1=$(openssl passwd -1 -salt bad4u Password1234)

awk -F: -v "awk_var=$var1" '{OFS=":"} {$2=awk_var} {print$0}' $HOME/PASS/shadow.txt
```
I create a variable at first. Then using awk I seperate on ":" and using awk variable substitution I create a variable within awk to call my created variable outside. I then call the second field of passwords to run my variable I created, which is what the ($2=awk_var) does, I then print the entire thing and the file I did this in was $HOME/PASS/shadow.txt

### Question ten

*Activity:
Using ONLY sed, write all lines from $HOME/passwd into $HOME/PASS/passwd.txt that do not end with either /bin/sh or /bin/false.*

```
sed '/\/bin\/sh/d' $HOME/passwd | sed '/\/bin\/false/d' $HOME/passwd  > $HOME/PASS/passwd.txt
```
this command uses sed to delete every line containing /bin/sh and /bin/false from the $HOME/passwd file and redirecting that into the newly created $HOME/PASS/passwd.txt file

### Question eleven

*Activity:
Using find, find all files under the $HOME directory with a .bin extension ONLY.
Once the file(s) and their path(s) have been found, remove the file name from the absolute path output.
Ensure there is no trailing / at the end of the directory path when outputting to standard output.
You may need to sort the output depending on the command(s) you use. Have each path displayed only once.*

```
find $HOME -type f -iname "*.bin" -printf "%h\n" 2>/dev/null | sort | uniq
```
This command finds every file (-type f) ending with the .bin extension (-iname "\*.bin") from within the $HOME directory, then we need to get rid of the file name from within the absolute path (-printf "%h\n") and then sorting the final product to only get the uniq ones we used (sort | uniq)

### Question twelve

*Activity:
Write a script that will do the following.
Write a script which will copy the last entry/line in the passwd-like file specified by the $1 positional parameter
Modify the copied line to change:
User name to the value specified by $2 positional parameter
Used id and group id to the value specified by $3 positional parameter
Home directory to a directory matching the user name specified by $2 positional parameter under the /home directory (i.e. if the $2 was 'Chris', the new line would have /home/Chris as its home directory)
The default shell to `/bin/bash'
Append the modified line to the end of the file*

```
tail -1 $1 | awk -v a=$2 -v b=$3 -F: '{OFS=":"} {$1=a;$3=b;$4=b;$6="/home/"a;$NF="/bin/bash";print$0}' >> $1
```
This command takes the last field within the $1 parameter. Then using awk creates new variables with the parameters set already (a=$2 and b=$3} seperating the entire line syntax with ":" using (OFS=":") then using variable subsitiution to get our required result and appending back to the original parameter ($1)

### Question thirteen

*Activity:
Find all executable files under the following four directories:
/bin
/sbin
/usr/bin
/usr/sbin
Sort the filenames with absolute path, and get the md5sum of the 10th file from the top of the list.*

```
fml=$(find /bin/ /sbin/ /usr/bin/ /usr/sbin/ -executable -type f | sort | head | tail -1)
md5sum $fml | awk '{print $1}'
```
This command creates a variable which runs through and finds every executable file within the directories listed and then get the 10th entry of the total sum of the files (sort | head | tail -1) then md5sums the file and prints the outcome using awk

### Question fourteen

*Activity:
Using any BASH command complete the following:
Sort the /etc/passwd file numerically by the GID field.
For the 10th entry in the sorted passwd file, get an md5 hash of that entry’s home directory.
Output ONLY the MD5 hash of the directory's name to standard output.*

```
sort -n -t ':' -k4 /etc/passwd | awk -F: 'NR == 10 {print $6}' | md5sum | cut -d' ' -f1
```
This command sorts numerically and on ":" (-n -t ':') gets only the GID field (-k4) of the /etc/passwd file then awks and delimites on every ":" (awk -F:) gets the 10th line (NR==10) and then prints ONLY the name of that specific entrys home directory (print $6) and then gets the md5sum hash of that and cuts off the ending of that hash using cut to get only the hash.

### Question fifteen

*Activity:
Write a script which will find and hash the contents 3 levels deep from each of these directories: /bin /etc /var
Your script should:
Exclude file type named pipes. These can break your script.
Redirect STDOUT and STDERR to separate files.
Determine the count of files hashed in the file with hashes.
Determine the count of unsuccessfully hashed directories.
Have both counts output to the screen with an appropriate title for each count.*

```
find /bin /etc /var -maxdepth 3 ! -type p -exec md5sum {} \; 1>file1  2>file2 

a=$(wc -l file1 | cut -d' ' -f1) 
b=$(egrep "directory" file2 | wc -l | cut -d' ' -f1)
echo "Successfully Hashed Files: $a"
echo "Unsuccessfully Hashed Directories: $b"
```
This command finds all files and directories 3 directories deep within the three directories called (-maxdepth 3) excluding al named pipes type files (! -type p) and then executing md5sum hash on every file (-exec md5sum {} \;) then sending every error output to file2 and every successfully hashed file and directory to file1

Then creating variables to run a wc list (wc -l) and cutting any white space on the hashes (cut -d' ' -f1) and then having an echo syntax to give the desired outcome calling our variables we just created

### Question sixteen

*Activity:
Design a script that detects the existence of directory: $HOME/.ssh
Upon successful detection, copies any and all files from within the directory $HOME/.ssh to directory $HOME/SSH and produce no output. You will need to create $HOME/SSH.
Upon un-successful detection, displays the error message "Run ssh-keygen" to the user.*

```
if [[ -d $HOME/.ssh ]];then
    cp -r $HOME/.ssh $HOME/SSH
else
    echo "Run ssh-keygen"
fi
```
This script runs if the $HOME/.ssh is a DIRECTORY (-d option) if so it copies recursively into the $HOME/SSH directory if not then it returns "Run ssh-keygen"

### Question seventeen

*Activity:
Write a script that determines your default gateway ip address. Assign that address to a variable using command substitution.
NOTE: Networking on the CTFd is limited for security reasons. ip route and route are emulated. Use either of those with no arguments/switches.
Have your script determine the absolute path of the ping application. Assign the absolute path to a variable using command substitution. HINT: man which
Have your script send six ping packets to your default gateway, utilizing the path discovered in the previous step, and assign the response to a variable using command substitution.
Evaluate the response as being either successful or failure, and print an appropriate message to the screen.*

```
A=$(route | grep 'UG[ \t]' | awk '{print $2}')
B=$(which ping)
C="$B -c6 $A"
D=$($C | grep "0%" | awk '{print $4}')
if [[ $D -eq '6' ]];then
    echo "successful"
else
    echo "failure"
fi
```

This script determines the default gateway address ($A) then setting the ping command ($B) and running that command against the default gateway ($C) then grepping for 0% knowing that if a 0% is received back with packets lost the ping was successful it returns "successful" if not it returns "failure"

### Question eighteen

*Activity:
Create the following files in a new directory you create $HOME/ZIP:
file1 will contain the md5sum of the text 12345
file2 will contain the md5sum of the text 6789
file3 will contain the md5sum of the text abcdef
Create a zip file containing the three files above, without being stored inside a directory in the zip file. Name the zip file $HOME/ZIP/file.zip
HINT: "Junk" the paths
Utilize tar on $HOME/ZIP/file.zip to archive it into a file called $HOME/ZIP/file.tar.gz which should not include directories. Use the gzip option in tar, DO NOT use a seperate gzip binary.
HINT: You might need an option to change directories first.*

```
DIR=$HOME/ZIP
ZIP=file.zip
TAR=file.tar.gz

cd $DIR || mkdir $DIR && cd $DIR

echo "12345" | md5sum | awk '{print $1}' > file1
echo "6789" | md5sum | awk '{print $1}' > file2
echo "abcdef" | md5sum | awk '{print $1}' > file3

zip -j file.zip *
tar czf file.tar.gz file.zip
```

### Question nineteen

*Activity:
Utilize Bash looping to iteratively create each user account and their directories.
Design a basic FOR Loop that iteratively alters the file system and user entries in a passwd-like file for new users: LARRY, CURLY, and MOE.
Each user should have an entry in the $HOME/passwd file
The userid and groupid will be the same and can be found as the sole contents of a file with the user's name in the $HOME directory (i.e. $HOME/LARRY.txt might contain 123)
The home directory will be a directory with the user's name located under the $HOME directory (i.e. $HOME/LARRY)
NOTE: Do NOT use shell expansion when specifying this in the $HOME/passwd file.
The default shell will be /bin/bash
The other fields in the new entries should match root's entry
Users should be created in the order specified*

```
rootline=$(head -1 $HOME/passwd)
for x in {LARRY,CURLY,MOE} ; do
   myuid=$(cat $HOME/$x.txt)
   mkdir $HOME/$x
   echo $rootline | awk -F: -v uu=$x -v ii=$myuid 'BEGIN{OFS=":"}{$1=uu;$3=ii;$4=ii;$6="$HOME/"uu}{print $0}' >> $HOME/passwd
done
```

### Question twenty

*Activity:
Write a bash script that will find all the files in the /etc directory, and obtains the octal permission of those files. The stat command will be useful for this task.
Depending how you go about your script, you may find writing to the local directory useful. What you must seperate out from the initial results are the octal permissions of 0-640 and those equal to and greater than 642, ie 0-640 goes to low.txt, while 642 is sent to high.txt.
Have your script uniquely sort the contents of the two files by count, numerically-reversed, and output the results, with applicable titles, to the screen. An example of the desired output is shown below.
NOTE: There is a blank line being printed between the two sections of the output below.*

EXAMPLE OUTPUT:

Files w/ OCTAL Perm Values 642+:
    424 777
    365 644
     15 755
  
Files w/ OCTAL Perm Values 0-640:
      4 640
      3 440
      2 600
      1 444

```
#!/bin/bash

find /etc -type f -exec stat -c '%a' {} \; 2>/dev/null 1>file1
for i in $(cat file1)
do
    if [[ $i -ge 642 ]];then
        echo $i >> high.txt
    else
        echo $i >> low.txt
    fi
done
a=$(sort high.txt | uniq -c | sort -r)
b=$(sort low.txt | uniq -c | sort -r)
echo "Files w/ OCTAL Perm Values 642+:
$a"
echo #this is set to create a blank space it does not print anything but a blank line to the screen
echo "Files w/ OCTAL Perm Values 0-640:
$b"
```

A find command is run to find the octal permissions of every file within the /etc directory and sending the outcomes to file1. A for statement is then run to iterate through that file using command substitution (for i in $(cat file1)) then an if statement is run so on the variable $i if it is greater then or equal to 642 its sent to the high.txt file and if its not its sent to the low.txt file. Then we set two more variables to sort and uniq both those files to call back in the echos for the final desired result.
