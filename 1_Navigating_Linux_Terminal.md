# Navigating the Linux Terminal

The Linux Terminal is the fastest way to navigate Linux systems, besides desktop environments provide you with a GUI, in most cases it is just way faster to do things on Terminal.

Let's start with the pure fundamentals of how to navigate the Terminal.

## Change directory

There is a command `cd` in Linux which stands for "Change Directory". This command is used constantly to navigate between different folders. If you type `cd` and then the folder name, you will change to this directory.

```
cd folder_name
```

You can `cd` into nested directories by adding additional directory names. You can use the "Tab" key on your keyboard to autocomplete your command, so you don't have to type the whole name.

```
cd folder_name/another_folder
```

It may happen that you change directories and you want to list the current directory path you are in. You can use `pwd` for this, which stands for "Print Working Directory".

```
pwd
```

In case you want to go back to your home directory, you can use `cd` without any argument, you will be redirected to your home.

```
cd
```

You can use the `~` symbol, which stands for the users home directory. In case you want to change directory based on your home folder, you can use this in any other subdirectory to move from home to your desired folder. In this case we move to the Downloads folder.

```
cd ~/Downloads
```

## Listing directories and files

With `ls` you can list the folder structure, files and folders, you are currently in.

```
ls
```

If you want more information on the files and folders, you can use `-l` to get it. The long list format includes file type, permissions, ownership, group, size, and also time and date.

```
ls -l
```

To also find out about hidden files and folders, you can add `-la` to list all available files and folders.

```
ls -la
```

If you only want to list folders but no files, you can use the `-ld */` command.

```
ls -ld */
```

In case you want to list files and/or folders including all subdirectories of the directory you are currently in, you can use `-R`. The following command displays all files and folders including subdirectories.

```
ls -l -R
```

If you want to list all files in a subdirectory of your current folder, you can specify the folder name after your `ls` command.

```
ls -l folder_name
```

You can also view the structure of a directory in a tree based structure, and the command is named `tree`. If you type it in a directory, it will give you a nice tree-like overview.

```
tree
```

## Clear or Reset Terminal

When you work in the Terminal, most of the times there is a lot going on and it is good to wipe out all information here and there.
You can use the `clear` or `reset` command to achieve this. I personally use `clear` all the time to get a clean looking Terminal again after doing some work.

```
clear
```
