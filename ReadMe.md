# Podman

# Table of contents
1. [Home](ReadMe.md)
1. [Podman Setup](PodmanSetup.md)
1. [Podman Commands](PodmanCommands.md)

## Description
---
Document to show the basic Podman setup and usage controls.

## Installation on Mac
---
Podman can be installed on Mac using [`brew`](https://brew.sh/) followed by the install command.

    brew install podman

- Linux containers require a Linux kernel, meaning running containers on a macOS requires a virtual machine running Linux.

- Podman on a macOS is not running containers locally on the macOS. The Podman command is actually communicating with the Podman service running on a Linux machine.

- The podman machine init command pulls down and installs a Fedora CoreOS VM onto your platform, which is running the Podman service.

- The podman machine init command also sets up the SSH environment required to allow the Podman remote client to communicate with the Podman server inside the VM.

## Installation on Windows
---

Podman can be install on Windows and uses WSL2.

    NOTE : WSL 1 doesn’t work with Podman; you must upgrade your Windows machine to an OS version that supports WSL 2. For x64 systems, you will need Windows version 1,903 or higher, with build 18,362 or higher. For arm64 systems, you will need Windows version 2004 or higher, with build 19,041 or higher.

Go to the Podman site or the Podman GitHub repository, and download the latest Podman MSI Windows Installer in the Releases

    https://github.com/containers/podman/releases

Also see how to :

- [Setup Podman on Windows](https://linh-b-ngo.medium.com/setup-podman-on-windows-c36fa5925403)

- [Run Podman on Windows: How-to instructions](https://www.redhat.com/sysadmin/run-podman-windows)

- [Podman Cheat Sheet](/tech-books-kindle/RedHatDeveloperEBooks/Podman-basics-cheat-sheet-Red-Hat-Developer.pdf)