# 01. Introduction to Linux

## What is Linux?

Linux is an open-source operating system (OS) kernel. When we say "Linux", we usually refer to a **Linux Distribution** (or Distro), which includes the kernel, system utilities, and applications.

- **Open Source:** The code is free to view, modify, and distribute.
- **Kernel:** The core of the OS that manages hardware (CPU, RAM, Devices).
- **Shell:** The interface (command line) that allows users to interact with the kernel.

## Linux vs. Windows vs. macOS vs. Android

| Feature                   | Linux                                 | Windows                      | macOS                                  | Android                                          |
| ------------------------- | ------------------------------------- | ---------------------------- | -------------------------------------- | ------------------------------------------------ |
| **Kernel**                | Linux Kernel (Monolithic)             | Windows NT Kernel (Hybrid)   | XNU (Hybrid, Unix-based)               | Linux Kernel (Modified/Monolithic)               |
| **Source Model**          | Fully Open Source (GPL)               | Closed Source (Proprietary)  | Partially Open (Darwin), mostly Closed | Open Source (AOSP) + Proprietary Google services |
| **File System Structure** | Unified tree (`/`)                    | Drive letters (`C:\`, `D:\`) | Unified tree (`/`)                     | Unified tree (`/`) with partitions               |
| **Default Shell**         | Bash, Zsh, Others                     | CMD, PowerShell              | Zsh                                    | Android Shell (via ADB)                          |
| **Package Management**    | `apt`, `yum`, `pacman`, `dnf`         | `winget`, Chocolatey         | Homebrew (3rd party)                   | Play Store, APKs                                 |
| **GUI Flexibility**       | Multiple DEs (GNOME, KDE, XFCE)       | Single Desktop Environment   | Single DE (Aqua)                       | OEM skins (OneUI, MIUI, ColorOS)                 |
| **Security Model**        | Strong permissions, RBAC              | UAC, ACL-based               | Unix-like permissions + sandboxing     | App sandboxing + permissions                     |
| **Virus/Malware Risk**    | Very Low                              | High                         | Low                                    | Medium                                           |
| **Performance**           | Lightweight, highly optimized options | Heavy, requires more RAM/CPU | Optimized for Apple hardware           | Varies by OEM/hardware                           |
| **Hardware Support**      | Wide community-driven support         | Extensive driver support     | Only Apple hardware                    | Runs on many OEM devices                         |
| **Software Installation** | Repos + source builds                 | `.exe`, MS Store             | `.dmg`, App Store                      | `.apk`, Play Store                               |
| **Developer Experience**  | Best for servers, DevOps, containers  | Strong .NET ecosystem        | Unix-based, stable dev tools           | Java/Kotlin mobile development                   |
| **Use Cases**             | Servers, cloud, DevOps, embedded      | Desktops, enterprise, gaming | Creative work, development             | Mobile devices, IoT                              |
| **Customization**         | Extremely high                        | Moderate                     | Very low                               | OEM-level customization                          |
| **Container Support**     | Native (Docker, LXC, Podman)          | Supported (Docker, WSL2)     | Supported (Docker)                     | Not common                                       |
| **System Updates**        | Fast, frequent                        | Large scheduled updates      | Controlled by Apple                    | Fragmented (depends on OEM)                      |
| **Cost**                  | Free                                  | Paid license                 | Hardware-locked                        | Free                                             |
| **File System Types**     | ext4, XFS, Btrfs, ZFS                 | NTFS, FAT32, exFAT           | APFS, HFS+                             | ext4, f2fs                                       |
| **Resource Footprint**    | Can run on minimal hardware           | Generally heavy              | Efficient but hardware-bound           | Varies widely                                    |

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
