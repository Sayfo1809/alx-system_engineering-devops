# 0x03. Shell, init files, variables and expansions

## 0-alias
The script creates an alias, with the following parameters:
> - name: __ls__
> - value: __rm *__
This is achieved using the **alias** command

`alias ls='rm *'`

## 1-hello_you 
The script prints **hello user**, where user is the current Linux user, using the **echo** command

`echo hello $USER`

## 2-path
The script adds **/action** to the **PATH**, such that */action* is the last directory the shell looks into when looking for a program. This is achieved using the **export** command

`export PATH=$PATH:/action`

## 3-paths
The script counts the number of directories in the PATH, using the **PATH** command in a pipeline.

`echo $PATH | tr -s ':' '\n' | wc -l`

## 4-global_variables
The scipt lists environment variables, using the **printenv** command

`printenv`

## 5-local_variables
The script lists all local variables and environment variables, and functions, using the **set** command

`set`

## 6-create_local_variable
The script creates a new local variable., with the following parameters:
> - name: __BEST__
> - value: __School__

`BEST='School'`

## 7-create_global_variable
The script creates a new global variable, with the following parameters:
> - name: __BEST__
> - value: __School__
This is achieved using the **export** command

`export BEST='School'`