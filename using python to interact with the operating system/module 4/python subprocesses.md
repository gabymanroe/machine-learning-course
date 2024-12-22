**Question 1**<br>
What type of object does a run function return?
- [ ] returncode
- [ ] stdout
- [ ] capture_output
- [x] CompletedProcess

**Question 2**<br>
How can you change the current working directory where a command will be executed?
- [x] Use the cwd parameter.
- [ ] Use the env parameter. 
- [ ] Use the shell parameter.
- [ ] Use the capture_output parameter.

**Question 3**<br>
When a child process is run using the subprocess module, which of the following are true? (check all that apply)
- [x] The child process is run in a secondary environment.
- [x] The parent process is blocked while the child process finishes.
- [ ] The parent process and child process both run simultaneously. 
- [x] Control is returned to the parent process when the child process ends. 

**Question 4**<br>
When using the run command of the subprocess module, what parameter, when set to True, allows us to store the output of a system command?
- [ ] cwd
- [x] capture_output
- [ ] timeout
- [ ] shell

**Question 5**<br>
What does the copy method of os.environ do?
- [x] Creates a new dictionary of environment variables
- [ ] Runs a second instance of an environment
- [ ] Joins two strings
- [ ] Removes a file from a directory
