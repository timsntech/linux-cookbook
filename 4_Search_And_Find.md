# Search and Find Files

It is important to be able to search and find files as well as search in files in your Linux Terminal.

## Search for Files

The main command to search for files in your Linux Terminal is the `find` command. This command allows you to find files on your system. There are multiple flags for this command, let's check them out.

#### Find files by name

If you want to find a file, you can specify several options. The command `find` gives you alle the options needed. This example will search for a file from the / directory with name file.txt.

```
find / -name file.txt
```

The above command is case sensitive, so in case you want to search case insensitive, you can do the following with `-iname`.

```
find / -iname File.txt
```

An example: This command checks if you have a file.txt in your Downloads folder.

```
find ~/Downloads -name file.txt
```

In case you want to find all files with an extension, you could do a `find` command like this:

```
find ~/Downloads -name "*.txt"
```

#### Find files by type

In case you don't want to search for the name of the file, but for the file type, you can also do that with the `find` command.
There are multiple options you can add to your search.
`f` stands for file, `d` stands for directory, `l` for symbolic link, `c` for character devices, `b` for block devices.
If you f.e. want to search for a specific folder in your Downloads folder, this is how it looks like.

```
find ~/Downloads -type d
```

#### Combine Search by type and name

If you want to combine searching for type and for name, you can run a command as the following, which searches in Downloads for for type file for all files with name ".txt" in it.

```
find ~/Downloads -type f -name "*.txt"
```

#### Find by file size

In case you want to search for a specific size, the `find` command allows us to do so. You can specify the `-size` option with a size. There are multiple size search options available, you can use `c` for bytes, `k` for kilobytes, `M` for megabytes, `G` for gigabytes, or `b` for 512-byte blocks. The following searches for all files from your / directory for files larger than 2000MB.

```
find ~/Downloads -size +50M
```

## Search in Files

You may want to search for content in certain files. A popular way of doing it is with the `grep` command.

This command will search for "search_term" in file.txt.

```
grep search_term file.txt
```

You can search in multiple files as well.

```
grep search_term file1.txt file2.txt file3.txt
```

To search in all files of a directory, you can use `grep` with an `*`

```
grep search_term *
```

If you want to find complete words only, there is a flag `-w` for "Word" that you can use:

```
grep -w search_term *
```

By default, `grep` is case sensitive, but you can tell it to ignore that, with `-i`.

```
grep -i search_term *
```

If you want to include all subfolders as well, you cann specify the `-r` flag.

```
grep -r search_term *
```

In cases where you want to search for complete strings, you can do that with the `-x` flag.

```
grep -x "this is my search_term" *
```

If you only want to get a list of files, where your search term is in, you can specifiy the `-l` flag.

```
grep -l search_term *
```

You can also search with the `less` command in the respective file. When you run `less`, type `/search_term` in the terminal (search_term is the word to search for) and it will show you where in the file this word appears.

```
less file.txt

# then in the terminal window, type this and press ENTER
/search_term

# this will highlight the words in the file in case they exist.
```
