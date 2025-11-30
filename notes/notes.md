# The Linux Command Line

## Introduction

### Why Use the Command Line?
> It's been said that “**graphical user interfaces make easy tasks easy**, while **command line interfaces make difficult tasks possible**” and this is still very true today.

### How To Read Book The Linux Command Line
> **Start at the beginning of the book and follow it to the end**. It isn’t written as a reference work, it's really more like a story with a beginning, middle, and end. 


### Why I Don't Call It “GNU/Linux”
> **“Linux” refers to the kernel** and all the other free and open source software found in the typical Linux distribution, that is, the entire Linux 
ecosystem, not just the GNU components.

---
---

## 1 - What Is the Shell

### What is the shell
> When we speak of the command line, we are really referring to the **shell**. 

> **The shell is a program that takes keyboard commands and passes them to the operating system to carry out.** Almost all Linux distributions supply a shell program from the GNU Project called 
bash. 

> The name “**bash**” is an acronym for “Bourne Again SHell”, a reference to the fact **bash is an** **enhanced replacement for sh**, the original Unix shell program written by **Steve Bourne**.

> **Terminal Emulators** provide the access to the shell.

---
---

## 2 - Navigation

- pwd – Print name of current working directory 
- cd – Change directory
- ls – List directory contents

> Unix-like systems such as Linux always have a single file system tree, regardless of how 
many drives or storage devices are attached to the computer. 

> Where an **absolute pathname** starts from the root directory and leads to its destination, a 
**relative pathname** starts from the working directory. 

> The "." notation refers to the working directory and the ".." notation refers to the working 
directory's parent directory

> In general, if we do not specify a pathname to something, the working directory will be assumed. In almost all cases, we can omit the "./". It is implied. 

### Important Facts About Filenames
- Filenames that begin with a period character are hidden.
- Filenames and commands in Linux, like Unix, are case sensitive. 
- Linux has no concept of a “file extension” like some other operating systems. The contents and/or purpose of a file is determined by other means. 
- limit the punctuation characters in the names of files you create to period, dash, and underscore. Most importantly, do not embed spaces in filenames. 

---
---

