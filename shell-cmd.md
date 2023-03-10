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


