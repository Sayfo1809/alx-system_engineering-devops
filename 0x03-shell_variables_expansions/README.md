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

## 8-true_knowledge
The script prints the result of the addition of 128 with the value stored in the environment variable **TRUEKNOWLEDGE**. this is achieved by means of the **echo** command.

`echo $((128 + $TRUEKNOWLEDGE))`

## 9-divide_and_rule
The script prints the result of **POWER** divided by **DIVIDE**, which are environment variables. This is achieved using the **echo** command.

`echo $(( $POWER / $DIVIDE ))`

## 10-love_exponent_breath
The script displays the result of **BREATH** to the power **LOVE**
> - BREATH and LOVE are environment variables
> - The script should display the result, followed by a new line
This is achieved using the **echo** command.

> `echo $(( $BREATH ** $LOVE ))`

## 11-binary_to_decimal
The script converts a number from base 2 to base 10.
> - The number in base 2 is stored in an environment variable, **BINARY**
> - The script should displays the number in base 10
This is achieved by using the **echo** command

`echo $(( 2#$BINARY ))`

## 12-combinations
The script prints all possible combinations of two letters, except oo.
> - Letters are lower cases, from a to z
> - One combination per line
> - The output should be alpha ordered, starting with aa

This is achieved by using a pipeline with the following steps
> 1. Print two letters
> 2. Trancate the results
> 3. Make sure the results does not include oo


`echo {a..z}{a..z} | tr ' ' '\n' | grep -v "oo"`

## 13-print_float
The script prints a number stored in the environment variable, **NUM** with two decimal places, using the **printf** command.

`printf '%.2f\n' $NUM`

## 100-decimal_to_hexadecimal
The script converts a number from base 10 to base 16.

> - The number in base 10 is stored in the environment variable, **DECIMAL**
This is achieved using the **printf** command.

`printf '%x\n' $DECIMAL`

## 101-rot13
The script encodes and decodes text using the rot13 encryption, making an assumption that ASCII is used. This is achieved using the **tr** command

`tr 'A-Ma-mN-Zn-z' 'N-Zn-zA-Ma-m'`

## 102-odd
The script prints every odd numbered lines from the input. This is achieved using the **paste** and **cut** commands in a pipeline.

`paste - - | cut -f1`