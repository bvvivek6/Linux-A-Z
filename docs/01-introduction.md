# 01. Introduction to Linux

## What is Linux?

Linux is an open-source operating system (OS) kernel. When we say "Linux", we usually refer to a **Linux Distribution** (or Distro), which includes the kernel, system utilities, and applications.

- **Open Source:** The code is free to view, modify, and distribute.
- **Kernel:** The core of the OS that manages hardware (CPU, RAM, Devices).
- **Shell:** The interface (command line) that allows users to interact with the kernel.

## Linux Architecture

Think of Linux as a layered cake:

1.  **Hardware:** The physical machine (RAM, HDD, CPU).
2.  **Kernel:** The "boss" that talks to the hardware.
3.  **Shell:** The "translator" that takes your commands and tells the kernel what to do.
4.  **Applications/Utilities:** Programs you run (web browser, text editor, `ls`, `cd`).

## The File System Hierarchy

Linux treats everything as a file. The file system is a tree structure starting from the root `/`.

| Path     | Description                                                                 |
| :------- | :-------------------------------------------------------------------------- |
| `/`      | **Root Directory**. The starting point of the file system.                  |
| `/bin`   | **Binaries**. Essential user command binaries (e.g., `ls`, `cp`).           |
| `/boot`  | **Boot Loader**. Files needed to boot the system.                           |
| `/dev`   | **Devices**. Device files (e.g., hard drives, terminals).                   |
| `/etc`   | **Etcetera**. Configuration files for the system.                           |
| `/home`  | **Home**. Personal directories for users (e.g., `/home/alice`).             |
| `/lib`   | **Libraries**. Shared libraries needed by binaries in `/bin` and `/sbin`.   |
| `/media` | **Media**. Mount points for removable media (USB, CD-ROM).                  |
| `/mnt`   | **Mount**. Temporary mount points.                                          |
| `/opt`   | **Optional**. Add-on application software packages.                         |
| `/proc`  | **Processes**. Virtual filesystem providing process and kernel information. |
| `/root`  | **Root Home**. The home directory for the root (admin) user.                |
| `/sbin`  | **System Binaries**. Essential system binaries (e.g., `reboot`, `fdisk`).   |
| `/tmp`   | **Temporary**. Temporary files (deleted on reboot).                         |
| `/usr`   | **User**. User utilities and applications (secondary hierarchy).            |
| `/var`   | **Variable**. Variable data files (logs, mail, spool).                      |

> **Key Takeaway:** Unlike Windows (C:\, D:\), Linux has a single tree structure starting at `/`.
