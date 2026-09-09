- Course: Complete Intro to Linux and the Command-Line
- Link: https://master.dev/courses/linux-command-line/
- Reference: https://btholt.github.io/complete-intro-to-linux-and-the-cli/

## Unix
Linux is considered a Unix-like operating system which basically means that Linux derives heavy inspiration from Unix without actually conforming to be a full Unix operating system. macOS and FreeBSD (a free and open-source Unix-like operating system derived from the Berkeley Software Distribution (BSD)) would be two more examples of a Unix-like operating system.

Again, _Linux isn't directly Unix_, just directly inspired by it, and incorporates many of its ideas and interfaces into it. It was created in **1991** by _Linus Torvalds_ who is still an influential figure today and still runs the Linux project. He created Linux because at the time there was no single free, open-source reimplementation of the Unix operating system (the BSD kernel wasn't yet available yet) so he wrote his own kernel which became known as the Linux kernel.

## Why Linux?
- First, it's free. Anyone can use Linux to do anything without paying anyone a dime. This is useful for college students who don't have any money but it's also critical for large businesses running thousands or tens-of-thousands of servers. It can save them millions of dollars to not have to pay for an operating system.
- It's very well maintained.
- It runs just about anywhere. Linux not only runs on x86 (the Intel / AMD processor architecture your computer is likely using) but it runs on Internet-of-Things devices, phones, fridges, cars, etc. If it has a processor in it, chances are you can get Linux running on it already.
- Most of the the things you need already exist for it.
- The knowledgebase for Linux is enormous (StackOverflow).

## What Makes Linux, Linux
At its core, Linux is the kernel. Anything based on this Linux kernel is a considered a Linux distribution, or distro for short.

## Virtualization
We're going to running our Linux through a process call virtualization. We'll be running a virtual machine which is frequently abbreviated as VMs. VMs are an operating system running within another operating system, called the host machine. The host machine will create a virtual environment with virtual acccess to its hardware to the VM. The VM will have no idea that it's not actually running on real hardware; all it can see is the resources that the host is providing it.

> [!NOTE]
> If you are on Windows 10 Home you need to install VirtualBox [link here](https://www.virtualbox.org/) too in addition to Multipass. Multipass will use VirtualBox if it can't use Microsoft Hyper-V (a feature only available in Windows 10 Pro.) If you are on macOS or Windows 10 Pro, you do not need VirtualBox.

## Anatomy of a CLI Command
- REPL, a Read Evaluate Print Loop, an interactive shell where you're writing one line of code at a time.
  This is the default of a shell

- You can run node or Python as a REPL as well.
  ```python
  ubuntu@befriended-horntail:~$ python3
  Python 3.14.4 (main, Jun 18 2026, 14:25:02) [GCC 15.2.0] on linux
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  ```
  `python` is already installed and you're running a REPL now for Python
- Linux is file system oriented, everything is a file in Linux.
- `pwd` stands for _print working directory_ or commonly referred to as __present working directory__

  > [!NOTE]
  > You're always somewhere in the file system at any given time.

## Shells vs. Emulators
- The **terminal** app inside of Mac is called the **emulator**. There are different **emulators** for Macs and Windows.
- The **emulator** can run any number of **shells**.
  You can have two tabs in the same **emulator**, one runs **bash** inside of Linux, the other runs **zsh** inside of Mac.
- The **emulator** is *different* from a **shell**, it contains the **shells** that are running.
- In this particular case, the **shell** is *bash*
  ```bash
  ubuntu@expansive-woodlouse:~$
  ```
  > [!NOTE]
  > **bash** is recommended for this course!
- If you do `--help` on the end of basically anything, it'll tell you how to use it
- `cd` - change directory
  - Say you're in the `ubuntu` directory and you want to go to `home` directory
  ```bash
  ubuntu@expansive-woodlouse:~$ pwd
  /home/ubuntu
  ubuntu@expansive-woodlouse:~$ cd /home
  ubuntu@expansive-woodlouse:~$ pwd
  ubuntu@expansive-woodlouse:/home$ pwd
  /home
  ```
  and say you want to go back to the `ubuntu` directory
  ```bash
  ubuntu@expansive-woodlouse:/home$ cd /home/ubuntu
  ubuntu@expansive-woodlouse:~$
  ```
  The faster way
  ```bash
  ubuntu@expansive-woodlouse:/home$ cd ..
  ubuntu@expansive-woodlouse:~$ pwd
  /
  ```
  You finally get to the root directory

  > [!TIPS]
  > `..` means *go up* once, `../..` means *go up* twice (directory). It's call the _relative path_
  > Learn more about [Command line crash course](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Environment_setup/Command_line)