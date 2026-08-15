<img width="2276" height="1183" alt="image" src="https://github.com/user-attachments/assets/0c8872c7-d60f-4fd5-800a-06754f8b0d69" /># Linux Basics

## Session 1

Today I installed Ubuntu in a VirtualBox virtual machine and practiced some basic Linux commands.

---

## pwd

Shows the current working directory.

Example:

```bash
pwd
```

Output:

```text
/home/abdulrahman
```

---

## ls

Lists the files and directories in the current location.

Example:

```bash
ls
```

Output:

```text
Desktop Documents Downloads Music Pictures Public Templates Videos snap
```

---

## mkdir

Creates a new directory.

Example:

```bash
mkdir cyberlab
```

---

## cd

Changes the current directory.

Example:

```bash
cd cyberlab
```

Output:

```text
/home/abdulrahman/cyberlab
```

---

## touch

Creates a new file.

Example:

```bash
touch notes.txt
```

---

## cat

Displays the contents of a file.

Example:

```bash
cat notes.txt
```

The file was empty, so no output was displayed.

---

---

# Shell and Bash Fundamentals

After learning the basic Linux command line, I started learning more about the shell and using Bash for scripting and automation.

## Shell

A shell is a program that allows me to interact with the operating system by entering commands.

Bash is one of the commonly used shells on Linux.

## Redirection

Redirection allows the input or output of commands to be redirected.

### Output Redirection

`>` writes the output of a command to a file.

```bash
echo "Hello" > file.txt
```

If the file already contains something, its contents are replaced.

`>>` appends the output instead of replacing the existing contents.

```bash
echo "Another line" >> file.txt
```

## Pipes

A pipe (`|`) sends the output of one command to another command.

```bash
ls | grep ".txt"
```

In this example, `ls` produces a list of files and `grep` searches that output for `.txt`.

This allows commands to be combined to perform more useful tasks.

## Variables

Bash variables can store values that can be reused later.

```bash
name="Abdulrahman"
echo "$name"
```

There should be no spaces around `=` when assigning a variable.

## User Input

The `read` command can be used to get input from the user.

```bash
read name
echo "Hello $name"
```

The value entered by the user is stored in the `name` variable.

## Conditionals

Conditionals allow a script to perform different actions depending on whether a condition is true or false.

```bash
if [ -f "notes.txt" ]; then
    echo "File exists"
else
    echo "File does not exist"
fi
```

This example checks whether `notes.txt` exists as a file.

## Loops

Loops allow commands to be repeated.

### For Loop

```bash
for file in *.txt
do
    echo "$file"
done
```

This loops through the `.txt` files in the current directory and prints each filename.

### While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo "$count"
    count=$((count + 1))
done
```

This repeats until `count` becomes greater than 5.

## Bash Scripts

Instead of entering commands individually, commands can be saved inside a Bash script.

A Bash script commonly uses the `.sh` extension.

Example:

```bash
#!/bin/bash

echo "Hello from Bash"
```

The first line:

```bash
#!/bin/bash
```

tells the system to use Bash to run the script.

## Making a Script Executable

A script can be given execute permission using:

```bash
chmod +x script.sh
```

It can then be executed with:

```bash
./script.sh
```

## Key Takeaways

- A shell provides a command-line interface for interacting with the operating system.
- Bash is both a shell and a scripting language.
- Redirection controls where command input and output go.
- Pipes allow the output of one command to become the input of another.
- Variables can store and reuse values.
- Conditionals allow scripts to make decisions.
- Loops allow commands to be repeated.
- Bash scripts can automate repetitive command-line tasks.
