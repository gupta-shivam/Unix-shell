Implementing a basic Shell 

Simple and thoroughly commented shell written in C by group 23
shivam gupta 150101068
shivram gowtham 150101069
shubham singhal 150101072

Features implemented :

Basic commands: pwd, clear,cd,ls

history n: it prints the last n commands entered.In history array we store all commands except history and issue command.
usage format: history 5

issue n: issues nth command from history.in issue command,if n >total no of commands till now,then it wont do anything.
usage format: issue 5

<program_name> write any program name,it will execute similar to linux bash.
usage format: firefox
usage format: cat file.txt

exit :it will exit this shell.

rmexcept command:to delete all files except a,b 
usage format: rmexcept a b

<program_name> m command: to abort process if dont complete in m secconds.
examples to test this command :  ping 202.141.80.24 5
								 firefox 5
these will end after 5 seconds

I/O redirection (use of dup2 system call) limited to the following format:
<cmd> <args> > <output>
<cmd> <args> < <input> > <output>

extra incentives:

Environment management:can print environment variables,set them or unset them.
usage format to print environment variables: environ
to set any environment variable: setenv varname value
to unset any environment variable: unsetenv varname

SIGINT signal when Ctrl-C is pressed (shell is not exited)


Shubham Singhal: 

* Wrote the code for <program name> m command using sigalarm and it's handler
* Wrote code for input output file direction using file descriptors

Shivam Gupta:
* Wrote the code for rmexcept <list of files> command
* Wrote code for running any <program name> using forking 

Shivram Gowtham:

* Wrote the code for managing environments (setenv , environ and unsetenv) using setenv system call 
* Wrote the code for cd , exit , clear and pwd.
