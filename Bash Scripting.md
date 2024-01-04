# Table of Content
[Definition of Bash scripting](#definition-of-bash-scripting)

[Advantages of Bash Scripting](#advantages-of-bash-scripting)

[Overview of Bash shell and command line interface](#overview-of-bash-shell-and-command-line-interface)

[How to Create and Execute Bash scripts](#how-to-create-and-execute-bash-scripts)

[Bash Scripting Basics](#bash-scripting-basics)

[Variables and data types in Bash](#variables-and-data-types-in-bash)

[Input and output in Bash scripts ](#input-and-output-in-bash-scripts)

[Conditional statements (if/else)](#conditional-statements-ifelse)

[Looping and Branching in Bash](#looping-and-branching-in-bash)




# Definition of Bash scripting
A bash script is a file containing a sequence of commands that are executed by the bash program line by line.
By saving these commands in a script, you can repeat the same sequence of steps multiple times and execute them by running the script.


# Advantages of Bash Scripting

## Efficient Automation:

Bash scripts automate repetitive tasks, saving time and reducing the risk of errors in manual execution.

## Platform Versatility:

Shell scripts run on various platforms like Unix, Linux, macOS, and even Windows, offering broad compatibility.

## Flexibility:

Highly customizable, shell scripts easily adapt to specific needs and can integrate with other languages for enhanced functionality.

## Accessibility and Simplicity:

Writing shell scripts is straightforward, requiring no special tools. They can be edited with any text editor and are supported by built-in shell interpreters on most operating systems.

## Seamless Integration:

Shell scripts integrate seamlessly with different tools and applications, enabling complex automation and system management.


# Overview of Bash shell and command line interface

The terms "shell" and "bash" are used interchangeably. But there is a subtle difference between the two.

The term "shell" refers to a program that provides a command-line interface for interacting with an operating system. Bash (Bourne-Again SHell) is one of the most commonly used Unix/Linux shells and is the default shell in many Linux distributions.

- A shell or command-line interface looks like this:


![](https://lh7-us.googleusercontent.com/ssPCdsGkUFELO6lzGjg2ctxizBK36tkWDxj8c-nqFbAuBKi6PUhhrHWuBA0ZA8kpffWDdXxX2v0zyXTb2erMBnmuIjrLby3PGseG-t0-NNkTXfMfvd60t4ATddTElbPvRE23vYo-VJ1PANsAbWheVEw)


- If the shell is running as root (a user with administrative rights), the prompt is changed to #. The superuser shell prompt looks like this:

![](https://lh7-us.googleusercontent.com/6GLWrqGevc21vxseEyXzK-3x0ruZRppKr0_EADx-hmTFiO5hpSxC8dspfNnaAfchYZztYKtet-Rq0pPH967-hsSjUn1kJUPnEcDMi3Z-5xCJ6dPmYb4Qh01hOxgLlAx50YwF-H2l-tdoHDBhDzau1rg)


Although Bash is a type of shell, there are other shells available as well, such as Korn shell (ksh), C shell (csh), and Z shell (zsh). Each shell has its own syntax and set of features, but they all share the common purpose of providing a command-line interface for interacting with the operating system.

# How to Create and Execute Bash scripts

## Script naming conventions

By naming convention, bash scripts end with .sh. However, bash scripts can run perfectly fine without the sh extension.

![](https://lh7-us.googleusercontent.com/3aw21RCJRkbJmxN4uASn_-tgO2OwuktyibI2yF0PimQvLtBgMbk4o8UbUjSwkjP1PxypYI92iFwMFB1mKHy7crmcTISVSIbuHK3LGXaWC8_z5S2L9aV826Wug7TcrZbZouFkONXo3ARcJWdyktMHjtM)



## Adding the Shebang

Bash scripts start with a shebang (#!/bin/bash). This is the first line of the script. Shebang tells the shell to execute it via bash shell. Shebang is simply an absolute path to the bash interpreter.



![](https://lh7-us.googleusercontent.com/ea4uLU8MDHZ--Ek6oSLWNG9xX4TT2GHnbT8M8Gz1qZ28ms52voizh1rE89kC4_iL34LGfUyzZMsrMR1pXgF5Ld54RcOdoHZd9bTPxQuHjU7luJzzdS7eeqFxpC0X_rSyPsS9_aVzxCkCHXkHQ-iphMI)



## Executing the bash script

To make the script executable, assign execution rights to your user using this command:


![](https://lh7-us.googleusercontent.com/Vsi8TZWTwAuy4XmNER2E6Sx6BvhR6DPWtvYbR16IojnPvFimtTnbzSauubKaW5-ozhSLp9M3cYxF-m2kLDWS1K04WxVNYygN8j6FDNJ-KmTX5JdBsMy9h_f6mMVGMQKrZ3UH9SExDNkO0UNaXM_9WzM)


# Bash Scripting Basics

## Comments in bash scripting
Comments start with # in bash scripting. This means that any line that begins with # is a comment and will be ignored by the interpreter.

Comments are very helpful in documenting the code, and it is a good practice to add them to help others understand the code.

These are examples of comments:



```
vim script_1.sh
```
```
#!/bin/bash

# this line is our comment
```

```
cat script_1.sh
```
```
chmod u+x script_1.sh
```


```
./script_1.sh
```

Output:-



Note:-
The script will not produce any output when it is run because the content has been commented out. Comments are ignored by the Bash interpreter, so they will not be executed.


# Variables and data types in Bash

Variables let you store data. You can use variables to read, access, and manipulate data throughout your script.

There are no data types in Bash. In Bash, a variable is capable of storing numeric values, individual characters, or strings of characters.

## Variable naming conventions
### In Bash scripting, the following are the variable naming conventions:

- Variable names should start with a letter or an underscore (_).
- Variable names can contain letters, numbers, and underscores (_).
- Variable names are case-sensitive.
- Variable names should not contain spaces or special characters.
- Use descriptive names that reflect the purpose of the variable.
- Avoid using reserved keywords, such as if, then, else, fi, and so on as variable names.

```
vim script_2.sh
```

```
#!/bin/bash

# this line is our comment

a=manish

echo “my name is $a”
```

```
cat script_2.sh
```
```
chmod u+x script_2.sh
```


```
./script_2.sh
```



## Output:-





# Input and output in Bash scripts 
## Gathering input
We can read the user input using the read command.

```
vim script_3.sh
```

```
#!/bin/bash

# this line is our comment

echo "Enter the name of the directory you want to create:"
read directory_name

mkdir -p "$directory_name"

```

```
cat script_3.sh
```
```
chmod u+x script_3.sh
```


```
./script_3.sh
```



## Output:-


# Basic Bash commands (echo, read, etc.)
## Here is a list of some of the most commonly used bash commands:

- cd: Change the directory to a different location.
- ls: List the contents of the current directory.
- mkdir: Create a new directory.
- touch: Create a new file.
- rm: Remove a file or directory.
- cp: Copy a file or directory.
- mv: Move or rename a file or directory.
- echo: Print text to the terminal.
- cat: Concatenate and print the contents of a file.
- grep: Search for a pattern in a file.
- chmod: Change the permissions of a file or directory.
- sudo: Run a command with administrative privileges.
- df: Display the amount of disk space available.
- history: Show a list of previously executed commands.
- ps: Display information about running processes.





# Conditional statements (if/else)
Expressions that produce a boolean result, either true or false, are called conditions. There are several ways to evaluate conditions, including if, if-else, if-elif-else, and nested conditionals.



## Syntax:
```
if [ condition ];
then
	statement
elif [ condition ]; then
	statement 
else
	do this by default
fi
```
```
vim script_4.sh
```

```
#!/bin/bash

# Script to create or check if a directory exists

echo "Enter the name of the directory you want to create:"
read directory_name

if [ -d "$directory_name" ]; then
  echo "Directory '$directory_name' already exists."
else
  mkdir -p "$directory_name"
  echo "Directory '$directory_name' created successfully."
fi

```
```
cat script_4.sh
```
```
chmod u+x script_4.sh
```


```
./script_4.sh
```




# Looping and Branching in Bash
## While loop
While loops check for a condition and loop until the condition remains true. We need to provide a counter statement that increments the counter to control loop execution.


```
vim script_5.sh
```

```
#!/bin/bash

# Your password is 1234
echo "Enter your password:"
read password

while [ $password -ne 1234 ]; do
    echo "The password $password is incorrect."
    echo "Enter the correct password:"
    read password
done

echo "Your password is correct."


```

```
cat script_5.sh
```
```
chmod u+x script_5.sh
```


```
./script_5.sh
```



## Output:-


## For loop
The for loop, just like the while loop, allows you to execute statements a specific number of times. 




```
vim script_6.sh
```

```
#!/bin/bash

# Define a prefix for the file names
prefix="file"

# Loop to create files file1.txt to file5.txt
for i in {1..5}
do
    filename="$prefix$i.txt"
    touch "$filename"
    echo "Created file: $filename"
done

```

```
cat script_6.sh
```
```
chmod u+x script_6.sh
```


```
./script_6.sh
```



## Output:-



## Case statements
Case statements are used to compare a given value against a list of patterns and execute a block of code based on the first pattern that matches. 


### The syntax for a case statement in Bash is as follows:
```
case expression in
    pattern1)
        # code to execute if expression matches pattern1
        ;;
    pattern2)
        # code to execute if expression matches pattern2
        ;;
    pattern3)
        # code to execute if expression matches pattern3
        ;;
    *)
        # code to execute if none of the above patterns match expression
        ;;
esac
```

```
vim script_7.sh
```

```
#!/bin/bash

echo "This is a menu:"
echo "Press 1. Check file and folder"
echo "Press 2. Create file"
echo "Press 3. Create folder"
echo "Press 4. Update system"

read choice

case $choice in
    1)
        ls
        ;;
    2)
        echo "enter your file name"
        read file_name
        touch $file_name
        ls
        ;;
    3)
        echo "enter your folder name"
        read folder_name
        mkdir $folder_name
        ls
        ;;
    4)
        sudo apt update
        ;;

    *)
        echo "Invalid choice. Exiting script."
        exit 1
        ;;
esac



```

```
cat script_7.sh
```
```
chmod u+x script_7.sh
```


```
./script_7.sh
```
