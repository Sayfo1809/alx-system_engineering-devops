# Shell I/O redirection projects

## 0-hello_world

The script prints “Hello, World” to the standard output, using the **echo** command

> `echo "Hello, World"`

## 1-confused_smiley

The script displays a confused smiley "(Ôo)' on the standard output, using the **echo** command

> `echo "\"(Ôo)'"`

## 2-hellofile

The script displays the content of the /etc/passwd file, using the **cat** command.

> `cat /etc/passwd`

## 3-twofiles

The script displays the content of /etc/passwd and /etc/hosts, using the **cat** command

> `cat /etc/passwd /etc/hosts`

## 4-lastlines

The script displays the last 10 lines of /etc/passwd, using the **tail** command

> `tail -n 10 /etc/passwd`

## 6-third_line

The script displays the third line of a file called iacta, contained in the working directory, using a piline of **head** and **tail**

> `head -n 3 iacta | tail -n 1`

## 7-file

The script creates a file named exactly **\*\\'"Best School"\'\\\*$\?\*\*\*\*\*:)** containing the text **Best School**, using **echo** command.

> `echo "Best School" >> "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"`

## 8-cwd_state

The script writes into the file **ls_cwd_content** the result of the command **ls -la**, overwriting it if it already exists. This is achieved using the Output redirect command **>**

> `ls -la > ls_cwd_content`

## 9-duplicate_last_line

The script duplicates the last line of the file iacta. This is achieved by retrieving the last line from the file _iacta_ and then redirecting the output back into the **iacta** file, making sure not to overwrite the file by making use of the **>>** redirect command

> `tail -n 1 iacta >> iacta`

## 10-no_more_js

The script deletes all the regular files (not the directories) with a **.js** extension that are present in the current directory and all its subfolders, using the **find** command.

> `find . -name "*.js" -delete`

## 11-directories

The script counts the number of directories and sub-directories in the current directory, icluding hidden directories. This is achived by pipelining the **find** and **wc** command

> `find . ./ -type d | wc -l`

## 12-newest_files

The script displays the 10 newest files in the current directory, using a pipeline of the **ls** and **head** command

> `ls -lt | head`

## 13-unique

The script takes a list of words as input and prints only words that appear exactly once. It is assumed that the list will be the first link of the pipe and then the script will join and complete the pipiline. The commands used are: **sort** and **uniq**

> `cat list`(assumed) `sort | uniq -u`
