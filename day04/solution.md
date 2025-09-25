
# Day 4 Answers: Basic Linux Shell Scripting for DevOps Engineers

Task 1: Explain in your own words and with examples what Shell Scripting means for DevOps.
- 'Shell scripting in DevOps simply means writing small programs (scripts) using shell commands to automate repetitive tasks like deployments, backups, monitoring, or server setup. Instead of running commands manually one by one, you write them in a script and let it run automatically, saving time and reducing errors. For example, instead of typing commands every day to back up logs, you can write a shell script that copies log files to a backup folder and schedule it with cron. This way, DevOps engineers can handle large-scale systems more efficiently and ensure processes are consistent and reliable.'

Task 2: What is `#!/bin/bash`? Can we write `#!/bin/sh` as well?
`#!/bin/bash` is called a shebang (#!) line in shell scripts. It tells the system which interpreter should be used to run the script.

- `#!/bin/bash` → runs the script using the Bash shell (Bourne Again SHell). Bash supports advanced features like arrays, [[ ]] for condition checks, better string handling, etc.

- `#!/bin/sh` → runs the script using the sh shell (Bourne shell or its compatible implementation). It’s more basic and works on almost all Unix/Linux systems, but lacks some Bash-specific features.

Task 3: Write a Shell Script that prints `I will complete #90DaysOfDevOps challenge`.

![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day04/image/task%203.png)

Task 4: Write a Shell Script that takes user input, input from arguments, and prints the variables.

![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day04/image/task%204(2).png)
![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day04/image/task%204.png)

Task 5: Provide an example of an If-Else statement in Shell Scripting by comparing two numbers.

![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day04/image/task%205.png)
