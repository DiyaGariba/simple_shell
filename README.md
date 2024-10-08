# simple_shell

MSH (Minimal Shell)

MSH is a minimalistic shell implementation that provides a basic command-line interface with enhanced features. This README outlines the various functionalities supported by MSH.
Table of Contents

    MSH (Minimal Shell)
        Table of Contents
            Change Directory (cd)
            Alias and Unalias
                Usage:
            Logical Operators (&& and ||)
                Example:
            System Commands
                Example:
            Exit Command
                Example:
            Setenv and Unsetenv
                Example:
            File as Input
                Example:
            Comments
                Example:
            Variable Expansion
                Example:
            Command Separator (;)
                Example:
            Custom Env
                Example:
            PATH
            Commands with and without Arguments
                Examples:
        Releases
        Download and Usage
        Author

Change Directory (cd)

The cd command is built into MSH, allowing users to change the current working directory. Simply enter cd [directory] to navigate to the specified directory. If [directory] is omitted, the current user's $HOME directory is used. This cd also handles the - argument that's passed to the cd command. For example, when the command is cd -, the shell changes directory to the value of $OLDPWD, which is the last directory the user visited before their current working directory.
Alias and Unalias

MSH supports aliasing commands for convenience using the alias command and removing aliases with unalias. This enables users to create shorthand notations for commonly used commands.
Usage:

alias cls='clear'
alias md=mkdir

# Improved usage
alias ls="ls --color=auto" ping="ping -c 5"
alias memchk='valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes -s'
alias flush_dns_cache=""
alias lsfwrules='sudo iptables -nv --line-numbers -L '
.
.
.
alias flush_dns_cache='resolvectl flush-caches'
alias l1="ls -1"
alias grep='grep --color=auto'

unalias cls # remove the 'cls' alias

Logical Operators (&& and ||)

Logical operators && (AND) and || (OR) are supported in MSH. They enable users to execute commands conditionally based on the success or failure of previous commands.
Example:

command1 && command2
command1 || command3

System Commands

MSH allows the execution of system commands. Enter any system command directly in the shell prompt to run it.
Example:

ls -a
cat /etc/passwd
mkdir src

Exit Command

The exit command, built into MSH, is used to exit the shell gracefully. It takes positive exit codes
Example:

exit
exit 1 # exit with status code 1

Setenv and Unsetenv

The setenv and unsetenv commands are utilized to set and unset environment variables, respectively. This feature enhances the customization of the shell environment.
Example:

setenv MY_VARIABLE my_value
unsetenv MY_VARIABLE

File as Input

MSH can take input from a file, allowing users to execute a series of commands from a script.
Example:

msh script.txt

Comments

Comments can be added to MSH using the # symbol, allowing users to annotate their commands without affecting execution.
Example:

# This is a comment
echo "Hello, MSH!"

ls # this will list the contents in the current working directory

Variable Expansion

MSH supports variable expansion, including $$ (current process ID) and $? (exit status of the last executed command).
Example:

echo "Process ID: $$"
command
echo "Exit Status: $?"

Command Separator (;)

The semicolon (;) acts as a command separator in MSH, allowing users to execute multiple commands on a single line.
Example:

command1 ; command2

Custom Env

Custom command env is available to display the current environment variables.
Example:

env

PATH

MSH uses the PATH environment variable to locate executable files. Ensure the desired directories are included in the PATH for seamless command execution.
Commands with and without Arguments

MSH supports commands with and without arguments, providing flexibility in command execution.
Examples:

ls
ls -l

Releases

    Latest Release
    All Releases

Download and Usage

To download the latest release of MSH, click here.

For information on how to install and execute, please visit the wiki
Author
Hamdiya Gariba
