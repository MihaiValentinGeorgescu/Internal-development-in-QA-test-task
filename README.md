# Internal-development-in-QA-test-task
created a program that synchronizes 2 folders.

This script is designed to copy all files and folders from a source directory to a destination directory, while 
also creating any subfolders that exist in the source directory.

The script starts by importing the necessary modules: os for file operations, shutil for file copying, and sys for command line arguments.
The logging variable is set to a default value of 'false' and determines whether or not the script will output logs. If logging is set 
to 'true', then the log() function will be called to output information about the script's progress.

The copy() function takes two arguments, path_src and path_des, representing the source file or folder to be copied and the destination 
to which it will be copied, respectively. If logging is set to 'true', then the function will output the paths of the source and destination 
files. The shutil.copy() function is used to perform the actual copy operation.

The each_file() function is the main function of the script, which takes two arguments, path_src and path_des, representing the source directory 
and destination directory, respectively. The os.walk() function is used to recursively traverse the source directory, and for each folder and subfolder 
encountered, the function creates a new folder in the destination directory using the os.mkdir() function. For each file encountered, the 
copy() function is called to copy the file from the source to the destination directory.

Finally, the script uses command line arguments to determine the source and destination directories. If the script is called with the 
argument "-d", then the current working directory is used as the source directory, and the destination directory is specified as the 
second command line argument. If the script is called with the argument "-s", then the current working directory is used as the destination 
directory, and the source directory is specified as the second command line argument.
