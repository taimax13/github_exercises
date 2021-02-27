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

To interact in powerful ways with folders and files using the command line, you need to know only a few basic commands. The basic tasks you can do are the same regardless of your operating system. However, the command you enter for a specific task will depend upon your operating system. 

Below is a list of basic commands to get started. Before you study it, here are a few notes to help you understand the commands. First, the word "directory" means "folder". Second, text wrapped inside `<` and `>` indicate a placeholder for a real folder, filename, or command.   

A few more tips you should know about are below, but this is enough to introduce you to some basic commands for interacting with folders and files. Here is a list of basic commands.  

| Description | Command (Windows)  | Command (Mac OS / Linux) | 	 
| ------------- | ------------- | ------------- |  
| Show filepath for the current directory	| cd	| pwd	|   
| List contents of pwd	| dir	| ls	| 
| Change the pwd |cd < directory_path >	| cd < directory_path >	|   
| Move pwd one directory up | cd.. | cd .. |  
| Create a new directory | mkdir < directory_path >	| mkdir < directory_path >	| 
| Delete a directory	|rmdir /s < directory_path >	| rm -r	< directory_path > |  
| Create new empty file | type nul > < file_path > | touch < file_path > | 
| Delete a file	|  del  < file_path > | 	rm < file_path > | 
| Copy file to dir or file	| copy < from_path > < to_path > 	| cp	< from_path > < to_path > |   
| Move file from one dir to another	| move < from_path > < to_path >	| mv < from_path > < to_path >	| 
| Rename file | rename  file_path  new_name |  mv < from_path > < to_path >	|
| Get help for a command	| < CMD > /?	| man < CMD > | 
| Clear the terminal screen | cls | clear | 

Note that filepaths for files (e.g., < file_path >) end with a file type. For instance, `.txt`, `.png`, `.js`, `.html`, and `.css`. For instance, when creating a new file, you could enter the following command:  

Windows
```terminal
> type nul > index.js
```

Mac and Linux
```terminal
$ touch index.js
```

In contrast, filepaths for directories do not end with a file type. For instance, when creating a new directory, you could enter the following command:  

Windows, Mac and Linux
```terminal
$ mkdir Code
```

Also note that you can use absolute or relative filepaths. An absolute filepath is the entire filepath needed to locate the folder or file on your computer, starting from the computer's root. A relative filepath, however, is only the filepath needed to locate the folder or file relative to your command line's present working directory. The present working directory is the folder the command line is currently pointing to.

Here's more about relative paths. To refer to a file in the pwd, you just need to call it by its name. To refer to a file in a subfolder of the pwd, you need the subfolder name, a `/`, and the file name. Here is an example of copying a file from the pwd and saving it in an existing folder in the pwd named `Bootcamp`. 

Windows
```terminal
copy index.js Bootcamp/index.js   
```

Mac and Linux
```terminal
cp	index.js Bootcamp/index.js
```

Notice that the path to `index.js` in the pwd and the path to `index.js` in `Bootcamp` are both relative paths. The relative path assumes the start is the pwd and the end is the name of the folder or file, and the in between are the folder names needed to connect the start to the end.  

Finally, two shortcuts. 

One, you can drag a folder from your computer's graphical user interface to the command line prompt. This results in the path to that folder. This is especially helpful when changing directories. You can type in your command line `cd`, then a space, and then drag the folder to the command line. Big time saver. 

Two, you can use the `Tab` key on your computer to autofill the name of a folder or file in the pwd. The autofill only works if the command line can tell by what you've already typed which folder or file you're referring to. For instance, if you have in your pwd folders named `Boots` and `Bootcamp`, if you type `cd Boot` and then `Tab`, nothing will happen. But if you type `cd Bootc` and then `Tab`, then the command line will autofill `cd Bootcamp/` for you.

## [Practice The Basics](#practice-the-basics)

Here is a step-by-step way to practice the basics. Follow the steps below using the command line, and after you will have some basic experience to do some powerful things quickly. You also will have a folder for storing all your development work. When you're done, take a screenshot of your terminal with the commands that you entered. Save that screenshot in your new development folder.

- Open the command line  
- Use **at least two** different commands to confirm your pwd is the desktop of your computer  
- Create a new directory on your Desktop and name it `Code`  
- Change your pwd to your new `Code` folder    
- Create a new folder inside `Code` and name it `Bootcamp`      
- Create another new folder inside `Code` and name it `Temporary`    
- Change your pwd to the `Temporary` folder   
- Create a file inside `Temporary` and name it `index.js`  
- Save a copy `index.js` in the `Bootcamp` folder  
- Change your pwd from the `Temporary` folder to your `Code` folder  
- Delete the `Temporary` folder     
- Take a screenshot of your terminal with the commands that you entered    
- Rename the screenshot to `command_basics.png` (or whatever file type you have)  
- Use the command line to move the screenshot to your `Bootcamp` folder    
- Change your `pwd` to the `Bootcamp` folder  
- List the contents of that folder to confirm your screenshot is there  
- Change the pwd from `Bootcamp` to one directory up 
- List the contents of the new pwd  
- Change your `pwd` to the `Bootcamp` folder  
- List the contents of that folder to confirm your screenshot is there  
- Change the pwd from `Bootcamp` to one directory up 
- List the contents of the new pwd 
- Change the pwd from `Code` to one directory up  
- List the contents of the new pwd 

## [Where To Find Commands For `git` And GitHub](#where-to-find-commands-for-git-and-github)  

