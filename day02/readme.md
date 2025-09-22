✅ Day 2 Tasks
Basic Linux Commands
Listing Commands
ls option_flag arguments


→ Lists the subdirectories and files available in the present directory.

Examples:

ls -l → List files and directories in long format with extra information.

ls -a → List all files including hidden ones.

ls *.sh → List all files having .sh extension.

ls -i → List files and directories with index numbers (inodes).

ls -d */ → List only directories (patterns can also be specified).

Directory Commands

pwd → Print working directory (shows the present directory).

cd path_to_directory → Change directory to the provided path.

cd ~ or just cd → Change directory to the home directory.

cd - → Go to the last working directory.

cd .. → Move one step back.

cd ../.. → Move two levels back.

mkdir directoryName → Create a directory in the specified location.

Examples:

mkdir newFolder              # make a new folder 'newFolder'

mkdir .NewFolder             # make a hidden directory ('.' before name makes it hidden)

mkdir A B C D                # make multiple directories at once

mkdir /home/user/Mydirectory # make a folder in a specific location

mkdir -p A/B/C/D             # make a nested directory


📅 Day 2 completed successfully!
Learned basic Linux commands for listing files and working with directories.