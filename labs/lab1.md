# [Lab Report 1 - Remote Access and FileSystem (Week 1)]
For each of the commands cd, ls, and cat, and using the workspace you created in this lab:

Share an example of using the command w
Share an exmaple of using the command with a path to a directory as an argument.
Share an example of using the command with a path to a file as an argument.

## Command "cd": 
 
1. No arguments: There is no error, after entering cd with no argument the command takes me back to home as shown below in the code block. The working directory before executing the command was "/home/lecture1". Please see code block below.
    
```console
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$
```
       
2. path to a directory as an argument: There was no error. The command takes the console into the lecture1 directory.  The working directory before executing the command was "/home". Please see code block below. 
    
```console
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```
       
3. path to a file as an argument: The working directory before executing the command was "/home". The error error was "lecture1/messages/en-us.txt: Not a directory". Please see code block below. The reason for this error is because a text file is not a directory
    
```console
[user@sahara ~]$ cd lecture1/messages/en-us.txt
bash: cd: lecture1/messages/en-us.txt: Not a directory
[user@sahara ~]$
```
       
       
## Command "ls" 

1. No arguments: The output after entering "ls" makes the console stay in the same directory. The working directory before executing the command was "/home". There ws no error. Please see code block below. 

~~~console
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
~~~

2. path to a directory as an argument: The command displays all the files and directories in the lecture1 directory. The working directory before executing the command was "/home". There ws no error. Please see code block below. 


~~~console
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$
~~~

3. path to a file as an argument: the command prints the path of the file. The working directory before executing the command was "/home". There ws no error. Please see code block below. 

```console
[user@sahara ~]$ ls lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
```

## Command "cat" 

1. No arguments: The command waits for an input, after typing a document name it just returns what i just typed. Using cat with no argument seems to just spit back what the user types. The working directory before executing the command was "/home/lecture1/messages". There ws no error. Please see code block below. 

~~~console
[user@sahara ~/lecture1/messages]$ cat
en-us.txt
en-us.txt
test
test
~~~

2. path to a directory as an argument: The command prints informs us that the thing we are trying to "cat" is a directory. The working directory before executing the command was "/home". There ws no error. Please see code block below. 

~~~console
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$
~~~

3. path to a file as an argument: the command prints out the content of the file "en-us.txt". The working directory before executing the command was "/home". There ws no error. Please see code block below. 

```console
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
[user@sahara ~]$
```


