# ALX Shell permissions exercise

## 0-iam_betty
The script switches the current user to the user betty, using the **su** command

>
`su betty`
>

## 1-who_am_i
The script prints the effective username of the current user, using the **whoami** command

>
`whoami`
>

## 2-groups
The script prints all the groups the current user is part of, using the **groups** command

>
`groups`
>

## 3-new_owner
The script changes the owner of the file hello to the user betty, using the **chown** command

>
`chown betty hello`
>

## 4-empty
The script creates an empty file called hello, using the **touch** command

>
`touch hello`
>

## 5-execute
The script adds execute permission to the owner of the file hello, using the **chmod** command

>
`chmod u+x hello`
>

## 6-multiple_permissions
The script adds execute permission to the owner and the group owner, and read permission to other users, to the file hello,contained in the working directory, using the **chmod** command

>
`chmod uh+x,o+r hello`
>

## 7-everybody
The script adds execution permission to the owner, the group owner and the other users, to the file hello, contained in the working directory, using the **chmod** command

>
`chmod a+x hello`
>

## 8-James_Bond
The script sets the permission to the file hello, such that:
    Owner: has no permission at all
    Group:has no permission at all
    Other users: has all the permissions

The file hello will be in the working directory. This is achieved using the **chmod** command

>
`chmod 007 hello`
>

## 9-John_Doe
The script sets the mode of the file hello to **-rwxr-x-wx**, using the **chmod** command

>
`chmod 753 hello`
>

## 10-mirror_permissions
The script sets the mode of the file **hello** using the mode of the file **olleh** as a reference. The hello and olleh files are contained in the same folder. This is achieved using the **chmod** command

>
`chmod --reference=olleh hello`
>

## 11-directories_permissions
The script adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other user, without changing the mode of regular files. This is achieved by searching for files in the current directory with a type d, and then apply a mode change to them, using the **chmod** command.

>
`chmod a+x $(find . -type d)`
>

## 12-directory_permissions
The script creates a directory called my_dir with permissions 751 in the working directory. This is achieved using the **mkdir** command

>
`mkdir -m 751 my_dir`
>

## 13-change_group
The script that changes the group owner to school for the file hello, contained in the working directory, using the **chgrp** command

>
`chgrp school hello`
>

## 100-change_owner_and_group
The script changes the owner to vincent and the group owner to staff for all the files and directories in the working directory, this is achieved by means of the **** command