---
description: Using Visual Studio Code for remote editing and debugging
ms.date: 11/16/2022
title: Using Visual Studio Code for remote editing and debugging
---
# Using Visual Studio Code for remote editing and debugging

For those of you that are familiar with the ISE, you may recall that you could run `psedit file.ps1`
from the integrated console to open files - local or remote - right in the ISE.

This feature is also available in the PowerShell extension for VS Code. This guide shows you how to
do it.

## Prerequisites

This guide assumes that you have:

- A remote resource (ex: a VM, a container) that you have access to
- PowerShell running on it and the host machine
- VS Code and the PowerShell extension for VS Code

This feature works on PowerShell and Windows PowerShell.

This feature also works when connecting to a remote machine via WinRM, PowerShell Direct, or SSH. If
you want to use SSH, but are using Windows, check out the [Win32 version of SSH][03]!

> [!IMPORTANT]
> The `Open-EditorFile` and `psedit` commands only work in the **PowerShell Integrated Console**
> created by the PowerShell extension for VS Code.

## Usage examples

These examples show remote editing and debugging from a MacBook Pro to an Ubuntu VM running in
Azure. The process is identical on Windows.

### Local file editing with Open-EditorFile

With the PowerShell extension for VS Code started and the PowerShell Integrated Console opened, we
can type `Open-EditorFile foo.ps1` or `psedit foo.ps1` to open the local foo.ps1 file right in the
editor.

![Open-EditorFile foo.ps1 works locally][04]

> [!NOTE]
> The file `foo.ps1` must already exist.

From there, we can:

- Add breakpoints to the gutter

  ![Adding a breakpoint to the gutter][05]

- Hit F5 to debug the PowerShell script.

  ![debugging the local PowerShell script][06]

While debugging, you can interact with the debug console, check out the variables in the scope on
the left, and all the other standard debugging tools.

### Remote file editing with Open-EditorFile

Now let's get into remote file editing and debugging. The steps are nearly the same, there's just
one thing we need to do first - enter our PowerShell session to the remote server.

There's a cmdlet for to do so. It's called `Enter-PSSession`.

In short:

- `Enter-PSSession -ComputerName foo` starts a session via WinRM
- `Enter-PSSession -ContainerId foo` and `Enter-PSSession -VmId foo` start a session via PowerShell
  Direct
- `Enter-PSSession -HostName foo` starts a session via SSH

For more information, see the documentation for
[Enter-PSSession][01].

Since we're remoting to an Ubuntu VM in Azure, we're using SSH.

First, in the Integrated Console, run `Enter-PSSession`. You're connected to the remote session when
`[<hostname>]` shows up to the left of your prompt.

![Call Enter-PSSession to connect to a remote session][07]

Now, we can do the same steps as if we're editing a local script.

1. Run `Open-EditorFile test.ps1` or `psedit test.ps1` to open the remote `test.ps1` file

   ![Edit the script on the remote system][08]

1. Edit the file/set breakpoints

   ![Edit and set breakpoints][09]

1. Start debugging (F5) the remote file

   ![Debugging the remote script][10]

If you have any problems, you can open issues in the [GitHub repo][02].

<!-- link references -->
[01]: /powershell/module/microsoft.powershell.core/enter-pssession
[02]: https://github.com/powershell/vscode-powershell
[03]: https://github.com/PowerShell/Win32-OpenSSH
[04]: media/Using-VSCode-for-Remote-Editing-and-Debugging/1-open-local-file.png
[05]: media/Using-VSCode-for-Remote-Editing-and-Debugging/2-adding-breakpoint-gutter.png
[06]: media/Using-VSCode-for-Remote-Editing-and-Debugging/3-local-debug.png
[07]: media/Using-VSCode-for-Remote-Editing-and-Debugging/4-enter-pssession.png
[08]: media/Using-VSCode-for-Remote-Editing-and-Debugging/5-open-remote-file.png
[09]: media/Using-VSCode-for-Remote-Editing-and-Debugging/6-set-breakpoints.png
[10]: media/Using-VSCode-for-Remote-Editing-and-Debugging/7-start-debugging.png
