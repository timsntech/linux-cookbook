# Managing Files and Directories

Besides of navigating the Terminal, you need to know how to create, edit, manipulate and delete files and folders.

## Create and Rename Files and Folders

To create a new folder, there is the `mkdir` command, which stands for "Make Directory". You need to pass a name for the directory you want to create.

```
mkdir my_folder_name
```

If you `ls` the folder will be there. You can `cd` into it.

To create a empty file, you can use the `touch` command. This will create a empty file with the name you specify for it. Later we will discuss how to edit files in your Terminal.

```
touch new_textfile.txt
```

You can create multiple files with one command.

```
touch file1.txt file2.txt file3.txt
```

Let's say you want to move a file or folder to a different folder. This can be done with `mv` command, which stands for "Move". To move a file or folder to another folder, you first type `mv`, then the file or folder to move, and then the directory to move the file to.

```
mv folder_to_move folder_to_move_to
```

You can also move multiple file or folders. The following command will move two files in a subdirectory.

```
mv file1.txt file2.txt folder_name
```

The `mv` is also used for renaming. To rename a existing file or folder, you type `mv`, then the file or folder to rename, and then the new name.

```
mv my_file.txt renamed_file.txt
```

## Copying Files and Folders

To copy files and/or folders, you can use the `cp` command, which stands for "Copy". It does exactly that. Specify the location and/or new file name.

```
cp file.txt file_copy.txt
```

You can copy also into other directories, if you add where to copy it to. Note, that the folder must exist.

```
cp file.txt subfolder/file_copy.txt

```

## Deleting Files and Folders

To delete a file, you can use the `rm` command. Note, this only works for files, if you add no flags.

```
rm file.txt
```

You can also remove multiple files.

```
rm file1.txt file2.txt file3.txt
```

To delete a folder, you can add the '-r' flag. The `-r` stands for recursive. The way it works is the `-r` deletes everything inside the folder and recursively each directory in it.

```
rm -r folder_name
```

You can also remove multiple folders.

```
rm -r folder_name1 folder_name1
```

For empty folders, you can also use `rmdir` command, which stands for "Remove Directory". Note, that the folder needs to be empty to remove it successfully.

```
rmdir empty_folder_to_remove
```

Another fast way to delete a folder with all its content is the `-rf` command. You need to be careful with it, because it will force deletion and if you accidentially delete your home or root directory it's gone. Better not use it at all ;-)

```
rm -rf folder_name
```
