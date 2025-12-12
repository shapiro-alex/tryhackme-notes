# Windows PowerShell

- designed for task automation and configuration management
- PowerShell = object-oriented (unlike other text-based command-line tools)
  - handles complex data types and interacts with system components more effectively
- lately expanded to support macOS and Linux

---

## The Power in PowerShell
- object = item with `properties` (characteristics) and `methods` (actions).
  - car might have:
    - properties like `Color`, `Model`, and `FuelLevel`
    - methods like `Drive()`, `HonkHorn()`, and `Refuel()`
- objects are fundamental units that encapsulate data and functionality
  - makes it easier to manage and manipulate information
- **cmdlet** - returns objects that retain their properties and methods
  - allows for more powerful and flexible data manipulation
  - does not require additional parsing of text
 
---

## Launching PowerShell
- can be launched in multiple ways on Windows
  - Start Menu: search `powershell`
  - Run dialog: `Win + R` -> `powershell`
  - File Explorer: type `powershell` in address bar
  - Task Manager: File -> Run new task -> `powershell`
- can also be launched from Command Prompt (`cmd.exe`)
  - type `powershell` and press Enter
- after launch:
  - `PS` prompt indicates PowerShell
  - opens in current working directory

---
## Cmdlets
- PowerShell commands are called **cmdlets**
- follow a **Verb-Noun** naming convention
  - verb = action
  - noun = object
- examples:
  - `Get-Content`
  - `Set-Location`
---

## Discovering Commands
- `Get-Command`
  - lists available cmdlets, functions, aliases, and scripts
- can filter by command type
  - example: `-CommandType Function`

---

## Getting Help
- `Get-Help`
  - shows usage, parameters, and descriptions
- supports additional options:
  - `-examples`
  - `-detailed`
  - `-full`
  - `-online`

---

## Aliases
- aliases are shortcuts for cmdlets
- useful for users familiar with traditional commands
- `Get-Alias`
  - lists all aliases
- examples:
  - `dir` → `Get-ChildItem`
  - `cd` → `Set-Location`

---

## Modules
- modules extend PowerShell functionality
- `Find-Module`
  - searches online repositories
  - supports wildcards (`*`)
- `Install-Module`
  - installs modules locally
  - may prompt if repository is untrusted

 ---

 ## Piping
- piping (`|`) sends output of one command to another
- common across command-line environments
- PowerShell pipes **objects**, not plain text
  - objects include data, properties, and methods

---

## Sorting Objects
- `Sort-Object`
  - sorts objects by a specified property
- example:
  - `Get-ChildItem | Sort-Object Length`
  - sorts files by size

---

## Filtering Objects
- `Where-Object`
  - filters objects based on conditions
- filter by property value:
  - `-eq` → equal
  - `-ne` → not equal
  - `-gt` → greater than
  - `-ge` → greater than or equal
  - `-lt` → less than
  - `-le` → less than or equal
- pattern matching:
  - `-like` → matches wildcard patterns

---

## Selecting Output
- `Select-Object`
  - selects specific properties
  - limits or refines output
- example:
  - `Get-ChildItem | Select-Object Name, Length`

---

## Searching Text
- `Select-String`
  - searches for text patterns in files
  - similar to `grep` or `findstr`
- supports regular expressions
