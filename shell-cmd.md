### Shell snippet commands : 

> This is a list of commands we can use in shell.

###### lists the files and directories in the current directory : 
```shell
ls
```

###### changes the current directory. For example, to move to the directory named "myfolder" in the current directory, you would type : 
```shell
cd myfolder
```

###### Print the current working directory: 
```shell
pwd
```

###### creates a new directory. For example, to create a directory named "newfolder" in the current directory, you would type : 
```shell
mkdir newfolder
```

###### Displays the contents of a file : 
```shell
cat file_name
```

###### Searches for a string in a file : 
```shell
grep
```

###### Changes the permissions of a file or directory : 
```shell
chmod
```

###### Executes a command with superuser privileges: 
```shell
sudo
```

###### To delete a file named "myfile.txt" in the current directory, you would type : 
```shell
rm myfile.txt
```


###### To delete a directory and all of its contents, you can use the -r flag, like this : 
```shell
rm -r myfolder
```


###### To copy a file named "myfile.txt" from the current directory to a directory named "myfolder" in the same directory, you would type : 
```shell
cp myfile.txt myfolder/
```


###### To copy a directory and all of its contents, you can use the -r flag, like this : 
```shell
cp -r myfolder mynewfolder/
```


###### To move a file named "myfile.txt" from the current directory to a directory named "myfolder" in the same directory, you would type : 
```shell
mv myfile.txt myfolder/
```


###### To move a directory and all of its contents, you can use the -r flag, like this : 
```shell
mv -r myfolder mynewfolder/
```

###### to create a file named "newfile.txt" in the current directory, you would type : 
```shell
touch newfile.txt
```

###### Display the manual page for a command or program : 
```shell
man 
```

###### Display text on the terminal : 
```shell
echo 
```

###### Display a list of previously executed commands : 
```shell
history  
```

###### Search for files in a directory hierarchy : 
```shell
find   
```

###### change directory to the user's home directory : 
```shell
 cd ~  
```

###### provides additional information about each file, including its permissions, ownership, file size, and creation time : 
```shell
 ls -l  
```

###### list of all files and directories in the current working directory, including hidden files and directories, with detailed information such as file permissions, ownership, size, and modification date/time. : 
```shell
ls -la 
```

######  list of all files and directories in the current working directory, including hidden files and directories, with detailed information such as file permissions, ownership, size, and modification date/time. However, instead of displaying the user and group names, it displays their numeric IDs. This can be useful in cases where the names are not important or cannot be displayed properly. : 
```shell
ls -an
```

###### create a new directory called "my_first_directory" in the "/tmp" directory, which is located in the root directory. : 
```shell
mkdir ~/../tmp/my_first_directory
```

###### change the current working directory to the previous working directory. : 
```shell
cd -
```

###### analyze the contents of the "iamafile" and try to determine its type. For example, it may identify the file as a text file, image file, or binary file. The output of the command will show the type of the file based on its contents. This can be useful in cases where the file extension is not available or not reliable in determining the file type. : 
```shell
file /tmp/iamafile
```

###### create a symbolic link called "ls" that points to the "/bin/ls" file. This means that when you run the "ls" command, it will execute the "ls" command and list the contents of the current directory. Symbolic links can be useful in cases where you want to create a shortcut or alias for a command or file. : 
```shell
ln -s /bin/ls __ls__
```

###### copy all files with the ".html" extension in the current directory to the parent directory "../", without overwriting any files with the same name. : 
```shell
cp -n *.html ../
```

###### move all files in the current directory whose names start with an uppercase letter to the "/tmp/u" directory. : 
```shell
mv [[:upper:]]* /tmp/u
```

###### delete all files in the current directory that end with a tilde (~) character. : 
```shell
rm *~
```

###### -p: It's an option used with the mkdir command to create parent directories if they don't already exist. : 
```shell
mkdir -p welcome/to/school
```

###### list all files and directories in the current directory, including hidden files, with additional information like file types, permissions, and file sizes, sorted alphabetically. : 
```shell
ls -map | sort

ls: It stands for "list" and is a command used to list files and directories.
-m: It's an option used with the ls command to separate file names with a comma.
-a: It's an option used with the ls command to list all files, including hidden files.
-p: It's an option used with the ls command to append a "/" to directories.
sort: It's a command used to sort lines of text alphabetically.
```


## shell - permissions

###### print the name of the current user. : 
```shell
whoami
```

###### switch to another user account or become a superuser (also known as "root"). : 
```shell
su root
```

>This command is commonly used for administrative purposes, where a user may need to perform tasks that require elevated privileges, such as managing system configurations or installing software packages. It is important to exercise caution when using the su command, as switching to the root account can potentially cause damage to the system if used improperly.


###### display the list of groups a user belongs to. : 
```shell
groups
```

###### change the ownership of a file or directory to a specified user or group. : 
```shell
chown betty hello
```
>In the command chown betty hello, the user is asking to change the ownership of the file named "hello" to the user account named "betty". If the user running the command has sufficient privileges, the ownership of the file will be changed to the specified user.


######  modify the permissions of a file or directory : 
```shell
chmod u+x hello
```
>The chmod command uses a combination of letters and numbers to specify the permissions to be set. The letter u represents the owner of the file, while +x means to add the execute permission. Alternatively, -x would remove the execute permission, and =x would set the execute permission only for the owner, and remove it for all others.

######  modify the permissions of a file or directory to user and group and owner: 
```shell
chmod ug+x,o+r hello
```
>the user is asking to add execute permission to the owner and group (represented by ug) of the file named "hello", and add read permission to others (represented by o). If the user running the command has sufficient privileges, the permissions of the file will be changed accordingly.


###### change the permissions of a file or directory : 
```shell
chmod +x hello
```
>the command chmod +x hello means "add execute permission for all users to the file named 'hello'". After running this command, any user on the system will be able to execute the hello file if they have permission to access it.

###### change the permissions of a file or directory : 
```shell
chmod 007

In the mode string 007, the first digit 0 represents the special permissions of the file, the second digit 0 represents the permissions for the owner, the third digit 7 represents the permissions for the group, and the fourth digit 7 represents the permissions for all other users.

The digits in the mode string represent the permissions as follows:

0: no permission
1: execute permission
2: write permission
3: write and execute permissions
4: read permission
5: read and execute permissions
6: read and write permissions
7: read, write, and execute permissions
So, the command chmod 007 hello means "set no permissions for the owner and group, and give read, write, and execute permissions for all other users to the file named 'hello'". This mode is generally not recommended since it gives full permissions to all other users on the system, which can be a security risk.
```

######  set the permissions of one file to be the same as another file : 
```shell
chmod --reference=olleh hello
```
>The --reference option is used to set the permissions of one file to be the same as another file.
So, the command chmod --reference=olleh hello means "set the permissions of the file named 'hello' to be the same as the file named 'olleh'". This will copy the permissions of the olleh file and apply them to the hello file.
Note that the olleh file must exist in the same directory as the hello file for this command to work. If the olleh file is located in a different directory, you will need to specify the full path to the olleh file in the command.

######  set the permissions of one file to be the same as another file : 
```shell
chmod -R +X .
```
>The -R option is used to apply the permissions recursively to all files and directories within the specified directory.
The +X option means "add execute permission for directories and files that already have execute permission".
The . at the end of the command specifies the current directory.
So, the command chmod -R +X . means "recursively add execute permission for directories and files that already have execute permission within the current directory".
This command will modify the permissions of all files and directories within the current directory and its subdirectories that already have execute permission. It is useful for making all directories executable, which can be necessary for some programs or scripts to work properly.

