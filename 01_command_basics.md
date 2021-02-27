# Command Basics

As a developer, it is important you know how to work with the command line. You will frequently use the command line to interact with your projects during development. For instance, you will commonly use the command line to install third-party software packages for your projects. 

As you saw in the previous lesson, you also will use the command line to interact with `git` and GitHub. Therefore, you should know some basics about working with the command line.

After reading this article, you will know:   

- What the [command line is](#what-is-the-command-line)  
- Where to [find the command line](#where-to-find-the-command-line)  
- How to use [basic commands](#basic-commands)
- Where to find [commands for `git` and GitHub](#where-to-find-commands-for-git-and-github)   

## [What Is The Command Line](#what-is-the-command-line)  

The command line is a text-based way to interact with the software, folders, and files on your computer. Instead of using a graphical user interface, you enter into a prompt the commands for creating, viewing, moving, and manipulating files on your computer. You also can install and uninstall software using the command line. The command line has many names, such as terminal, cmd, CLI, prompt, and console.  

At first, using the command line might feel slow and awkward. You don't know the commands, so you spend time researching how to do even the simplest of things. Plus, the feel and experience of using the command line is different from using the graphical user interface like you're used to. However, the more you use the command line, the faster you'll get. You'll start to memorize commands and feel at home using it. 

Many people find the command line to be faster and more comfortable than using the graphical user interface for many tasks. For instance, you can rename a large number of files quickly using the command line, whereas it would take a long time to rename them using the graphical user interface.  

The commands you use differ based on the operatring system you use and too many exist for you to memorize. In this course, however, you will learn some of the important commands to know, which will be ones you will use on a regular basis. Plus, StackOverflow has a lot of great answers. Regardless, in case you need them, here is a list of [commands for Windows users](https://www.computerhope.com/msdos.htm) and a list of [commands for linux and unix users](https://www.computerhope.com/unix.htm).  

## [Where To Find The Command Line](#where-to-find-the-command-line)  

You already have the command line on your computer. The software comes with the operating system. How to find the command line depends on which operating system your computer runs. 

For Windows users, look for the **Command Prompt**. You can [find it in several ways](https://tutorial.djangogirls.org/en/intro_to_command_line/#open-the-command-line-interface). One way is to open the Start menu → Windows System → Command Prompt.  

For Mac and Linux users, look for the **Terminal**. You can [find the Terminal](https://tutorial.djangogirls.org/en/intro_to_command_line/#open-the-command-line-interface) in Applications → Utilities → Terminal.  

Once open, you should see a window with a line containing some text. That text is the filepath of where on your computer the command line is currently active. When you first open the command line like described above, you should probably see a filepath containing the name of your computer, the username of the computer user, and a `$` or `>`. This means the command line is pointed to the root folder for that user on your computer. To help explain, look at the contents in that folder. 

In your command line, if on a Windows machine, type `dir` and if on a Mac or Linux type `ls`. Then hit enter. Like the following:

- Windows
```terminal
> dir
```

- Mac or Linux
```terminal
$ ls
```

You should see the terminal print a list of folders and files located in the folder that the command line is pointing to. Does that list look familiar to you?

## [Basic Commands](#basic-commands)  

To interact in powerful ways with folders and files using the command line, you need to know only a few basic commands. The basic tasks you can do are the same regardless of your operating system. However, the command you enter for a specific task will depend upon your operating system. Here is a list of basic commands to get started. Note that "directory" is a folder and use of `<` and `>` indicate a placeholder for a real folder or filename.
 
| Command (Windows)  | Command (Mac OS / Linux) | Description |	 
| ------------- | ------------- | ------------- |  
| cd <path_to_directory>	| cd <path_to_directory>	| change directory |  
| cd	| pwd	| show the full filepath for the current directory	|  
| dir	| ls	| list directories/files	| dir | 
| cd.. | cd .. | move one directory up | 
| mkdir < directory_name >	| mkdir < directory_name >	| create a new directory |
| type nul > < directory_name > | touch < directory_name > | create new empty file |
| del  < file_name > | 	rm < file_name > | delete a file	| 
| rmdir /s < directory_name >	| rm -r	< directory_name > | delete a directory	| 
| copy < source_filepath > < destination_filepath > 	| cp	< source_filepath > < destination_filepath > | copy file to dir or file	|  
| move < source_filepath > < destination_filepath >	| mv < source_filepath > < destination_filepath >	| move file	| 
| CMD /?	| man CMD | get help for a command	|
| cls | clear | clear the terminal screen |

## [Where To Find Commands For `git` And GitHub](#where-to-find-commands-for-git-and-github)  

