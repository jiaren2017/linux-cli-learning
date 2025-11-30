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

## 3 - Exploring the System

- ls – List directory contents 
- file – Determine file type and print a brief description of the file's contents. 
- less – View file contents

### **command -options arguments**
> Commands are often followed by one or more options that modify their behavior, and further, by one or more arguments, the items upon which the command acts.

> **Note that command options, like filenames in Linux, are case-sensitive.**

### What Is “Text”
> **Text is a simple one-to-one mapping of characters to numbers.**
> ASCII text files contain only the characters themselves and a few rudimentary control codes such as tabs, carriage returns and line feeds.

### Directories on Linux Systems
| Directory   | Comments |
| :----- | :-------|
|/ |   The root directory. Where everything begins. |
|/bin |   Contains binaries (programs) that must be present for the system to boot and run.  |
|/boot |  Contains the Linux kernel, initial RAM disk image (for drivers needed at boot time), and the boot loader. |
|/dev |  This is a special directory that contains device nodes. “Everything is a file” also applies to devices. |
|/etc  |  The /etc directory contains all of the system-wide configuration files. Everything in this directory should be readable text. |
|/home  |  In normal configurations, each user is given a directory in /home. Ordinary users can only write files in their home directories. |
|/lib |  Contains shared library files used by the core system programs.  |
|/mnt  | contains mount points for devices that have been mounted manually. |
|/proc | It is a virtual file system maintained by the Linux kernel.
|/root | This is the home directory for the root account. |
|/run | This is a modern replacement for the traditional /tmp directory (see below). Unlike /tmp, the /run directory mounted using the tempfs file system type which stores contents in memory rather than on a physical disk. |
|/sbin | This directory contains “system” binaries. These are programs that perform vital system tasks that are generally reserved for the superuser.  |
|/sys |The /sys directory contains information about devices that have been detected by the kernel. |
|/tmp |The /tmp directory is intended for the storage of temporary, transient files created by various programs.  |
|/usr |It contains all the programs and support files used by regular users. |
|/usr/bin |/usr/bin contains the executable programs installed by the Linux distribution. |
|/usr/lib  |The shared libraries for the programs in /usr/bin.  |
|/usr/local  |The /usr/local tree is where programs that are not included with the distribution but are intended for system-wide use are installed. Programs compiled from source code are normally installed in /usr/local/bin.  |
|/usr/sbin  | Contains more system administration programs. |
|/usr/share  |/usr/share contains all the shared data used by programs in /usr/bin.  |
|/var | The /var directory tree is where data that is likely to change is stored. Various databases,  spool files, user mail, etc. are located here.|
|/var/log |  /var/log contains log files, records of various system activity. The most useful ones are /var/log/messages and/or /var/log/syslog |
|~/.config ~/.local| These two directories are located in the home directory of each desktop user. They are used to store user-specific configuration data for desktop applications. |

### Symbolic Links
> This is a **special kind of a file** called a symbolic link (also known as a **soft link** or **symlink**). In most Unix-like systems **it is possible to have a file referenced by multiple names.** 

> Suppose we install version 2.6 of “foo” which has the filename “**foo-2.6**” and then create a symbolic link simply called “**foo**” that points to “**foo-2.6**”. This means that when a program opens the file “**foo**”, it is actually opening the file “**foo-2.6**”. 

> When it is time to upgrade to “**foo-2.7**”, we just add the file to our system, delete the symbolic link “**foo**” and create a new one that points to the new version. 

> Imagine that “**foo-2.7**” has a bug (damn those developers!) and we need to revert to the old version. Again, we just delete the symbolic link pointing to the new version and **create a new symbolic link pointing to the old version**. 

---
---
