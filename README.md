Author: Abhisek Mohapatra
Email: amohapat1@stevens.edu

Minishell is a simple UNIX shell implementation written in C. It provides a basic command-line interface for users to interact with the operating system.

Bugs and Issues

    Currently, there are no known bugs or issues in the program.

Resolved Bug

During the development of the minishell, I encountered a bug where the background processes were not being properly reaped, leading to zombie processes. This issue was resolved by implementing a signal handler for SIGCHLD and calling waitpid with WNOHANG option to reap all child processes.
Question: Why are exit and cd built-in commands?

exit and cd are built-in commands in the minishell because they directly affect the state of the shell itself.

    exit: Exiting the shell terminates the entire shell process. If exit were implemented as an external executable, it would have to be run in a subprocess, and when that subprocess exits, it would not affect the main shell process. By making exit a built-in command, we ensure that it has direct control over the shell process.

    cd: Changing directories (cd) affects the working directory of the shell process. If cd were implemented as an external executable, it would change the directory of its own subprocess, not affecting the main shell process. Making cd a built-in command allows it to directly modify the state of the main shell process.
