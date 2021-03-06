# Get the Script

Clone the repository into your working directory with this command

```
$ git clone https://github.com/danieltriestocode/nasm_script.git < ~/PATH/TO/DIRECTORY >
```

<br />

# Guide

When you run the script you will be prompted with something like this

```
Exit the script with: Ctrl + C

1. asm_file1.asm
2. asm_file2.asm
3. asm_file3.asm

Enter: 
```

You only have to enter one command for this script

```
Enter: e 1 2
```

or 

```
Enter: d 1 2
```

## Explanation

`e` = execute 

`d` = debug

`1` = the first file listed in prompt

`2` = the second file listed in prompt

<br />

The order in which you put the files does not matter, so I could've instead put 

```
Enter: e 2 1
```

However, your first character should always be: `e` or `d`

## Shortcut

Entering a command with no selected files from the list will assume that you want all files within the current directory to be executed or debugged

```
Enter: e
```

is the same as (if we use the example above)

```
Enter: e 1 2 3
```

The same goes for debugging: `d`

<br />

# Including Library Files

You can include multiple library files by declaring them in your MAIN file

```
; lib: name_of_library.asm
```

Make sure to use `lib:` followed by a space with the name of your library file


You can include multiple files as well, just use the `lib:` keyword for each of them 

```
; lib: library1.asm
; lib: library2.asm
; lib: library3.asm
```

Before you start including library files, include the directory your library files are in on line `3`

```
3   lib_dir="$HOME/PATH/TO/LIBRARY/FOLDER"
```

### Example

```
3   lib_dir="$HOME/Desktop/CSCI_150/library_dir"
```

<br />

# Other Commands 

`c` = clear screen

`↑↓` = go through input history

`<empty>` = execute/debug the last acceptable command of that session

`h` = display input history

`ch` = clear input history

<br />

# Video Examples: 

https://user-images.githubusercontent.com/100104016/179667430-df1aba73-e104-45bd-bc34-298978a0c0c9.mp4

https://user-images.githubusercontent.com/100104016/179667674-94270b35-193f-472b-a1a9-9fdc35408466.mp4
