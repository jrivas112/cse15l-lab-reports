# [Lab Report 1 - Remote Access and FileSystem (Week 1)]
For each of the commands cd, ls, and cat, and using the workspace you created in this lab:

Share an example of using the command w
Share an exmaple of using the command with a path to a directory as an argument.
Share an example of using the command with a path to a file as an argument.

## Command "cd": 
 
1. No arguments: The output after entering "cd" makes the console stay in the same directory 
    
```console
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
       
2. path to a directory as an argument: The command takes the console into the lecture1 directory
    
```console
[user@sahara ~/lecture1]$ 
```
       
3. path to a file as an argument: the command returns an error because en-us.txt is not a directory
    
```console
[user@sahara ~]$ cd lecture1/messages/en-us.txt
bash: cd: lecture1/messages/en-us.txt: Not a directory
[user@sahara ~]$
```
       
       
## Command "ls" 

1. No arguments: The output after entering "ls" makes the console stay in the same directory

~~~console
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
~~~

2. path to a directory as an argument: The command displays all the files and directories in the lecture1 directory

~~~console
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$
~~~

3. path to a file as an argument: the command prints the relative path of the file

```console
[user@sahara ~]$ ls lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
```

## Command "cat" 

1. No arguments: The command waits for an input

~~~console
[user@sahara ~/lecture1/messages]$ cat
~~~

2. path to a directory as an argument: The command prints informs us that the thing we are trying to "cat" is a directory

~~~console
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$
~~~

3. path to a file as an argument: the command prints out the content of the file "en-us.txt"

```console
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
[user@sahara ~]$
```


