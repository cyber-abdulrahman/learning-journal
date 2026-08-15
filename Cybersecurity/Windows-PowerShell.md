# Windows PowerShell

Notes from learning and practicing Windows PowerShell through TryHackMe.

## PowerShell Basics

PowerShell is a command-line shell and scripting environment used for Windows administration and automation.

Unlike traditional command-line tools that mainly work with text, PowerShell commands can pass objects between commands.

## Cmdlets

PowerShell commands are commonly called cmdlets and usually follow a `Verb-Noun` naming format.

Examples:

```powershell
Get-Process
Get-Service
Get-Content
```

The verb describes the action, while the noun describes what the command acts on.

## Getting Help

PowerShell provides built-in commands for learning about other commands.

```powershell
Get-Help Get-Process
```

Commands can also be discovered using:

```powershell
Get-Command
```

## Navigating the File System

PowerShell can be used to navigate and work with files and directories.

```powershell
pwd
ls
cd
```

## Working With Files

PowerShell provides commands for creating, reading, copying, moving, and deleting files.

Examples:

```powershell
New-Item
Get-Content
Copy-Item
Move-Item
Remove-Item
```

## Pipes

The pipeline operator (`|`) sends the output of one command to another command.

```powershell
Get-Process | Sort-Object CPU
```

This makes it possible to combine commands to filter, sort, or process information.

## Filtering Output

PowerShell can filter objects based on their properties.

```powershell
Get-Service | Where-Object {$_.Status -eq "Running"}
```

This example displays services that are currently running.

## System Information

PowerShell can be used to inspect information about a Windows system, including processes, services, users, files, and system configuration.

Examples:

```powershell
Get-Process
Get-Service
```

These commands are useful when investigating or administering a Windows machine.

## PowerShell in Cybersecurity

PowerShell is useful in cybersecurity because it provides access to Windows system information and administrative functionality.

Being comfortable with PowerShell can help with:

* System investigation
* Process and service inspection
* File system navigation
* Automation
* Windows administration

## Key Takeaways

* PowerShell is both a command-line shell and scripting environment.
* Cmdlets commonly use the `Verb-Noun` naming convention.
* `Get-Help` and `Get-Command` are useful for discovering and understanding commands.
* PowerShell pipelines can pass objects between commands for filtering and processing.
* PowerShell can be used to inspect processes, services, files, and other Windows system information.
* These capabilities make PowerShell useful for Windows administration and cybersecurity tasks.
