# Reading and Viewing and Searching Files

When working with Linux Terminal it is common to view, print and read files on your system.

## Print File Content

There are multiple ways and commands how you can access and read file content of a given file. All of the commands below allow you to read files, the commands just behave in different ways.

#### cat

The `cat` command is a popular command and displays the content of a file.

```
cat file.txt

# *** prints out file content***
```

#### more

If your file has a lots of content and many lines, it is better to use a command like `more`. This will print the file in smaller sections and you can skip through the results with ENTER. You can press SPACE to leave.

```
more file.txt

# when you have long files, the command will show:
# --- more ---
# and you can skip through the lines.
```

#### less

The `less` is pretty similar to the `more` command, but is a bit faster. It does not read the whole file till it displays the output. You can quit/close the window by typing `q` on your keyboard.

```
less file.txt

# when you have long files, the command will show:
# --- more ---
# and you can skip through the lines.
```

#### head

If you only want to view the first few lines of a file, the `head` command comes in handy. By default it displays the first 10 lines of the file. You can specify more lines with a flag.

```
# prints first 10 lines
head file.txt

# prints first 20 lines
head -20 file.txt
```

#### tail

The `tail` command does exactly the same as the `head` command, just the other way round. You can view the first few lines from the bottom of the file.

```
# prints last 10 lines
tail file.txt

# prints last 20 lines
tail -20 file.txt
```
