# advance Linux Commands

# File Permissions and Access Rights
Understanding File Permissions in Linux is crucial for maintaining security and proper access control. Each file and directory has associated permissions that determine who can read, write, or execute them.

In Linux, managing file permissions and ownership is essential for system security and user access control. The `chmod`, `chown`, and `chgrp` commands are used to modify permissions and ownership of files and directories.

# Numeric Representation of Permissions
Permissions can be represented numerically, where each permission is assigned a specific value:
- Read (r) = 4
- Write (w) = 2
- Execute (x) = 1
- No permission (-) = 0

These values are combined to represent the permissions for each class. for example:

## Permissions Represented by 7

- 4(read) + 2(write) + 1(execute) = 7
- Symbolic: rwx
- Meaning: Read, Write, and Execute permissions are granted.
- Example Context: A script file that the owner needs to read, modify, and execute.
- 
## Permissions Represented by 5
- 4(read) + 1(execute) = 5
- Symbolic: r-x
- Meaning: Read and Execute permissions are granted, but Write permission is denied.
- Example Context: A directory where users can list files and execute programs but cannot modify the contents.
  
## Permissions Represented by 6
- 4(read) + 2(write) = 6
- Symbolic: rw-
- Meaning: Read and Write permissions are granted, but Execute permission is denied.
- Example Context: A configuration file that needs to be read and modified by the owner but not executed.
  
## Permissions Represented by 4
- 4(read) = 4
- Symbolic: r--
- Meaning: Only Read permission is granted.
- Example Context: A log file that users can read but not modify or execute.    
  
## Permissions Represented by 0
- 0(no permissions) = 0
- Symbolic: ---
- Meaning: No permissions are granted.
- Example Context: A sensitive file that should not be accessible to anyone.
## Permissions Represented by 1
- 1(execute) = 1
- Symbolic: --x
- Meaning: Only Execute permission is granted.
- Example Context: A binary file that can be executed but not read or modified.     
## Permissions Represented by 2
- 2(write) = 2
- Symbolic: -w-
- Meaning: Only Write permission is granted.
- Example Context: A temporary file that can be modified but not read or executed.  
## Permissions Represented by 3
- 3(write + execute) = 3
- Symbolic: -wx
- Meaning: Write and Execute permissions are granted, but Read permission is denied.        
- Example Context: A script that can be modified and executed but not read by others.   

## Shorthand Representation of Permissions
In addition to the numeric representations, Linux also has a shorthand, or symbolic, method for representing file permissions.

## Understanding User Classes from a Permission Perspective
Linux file permissions are divided into three user classes:
- **Owner**: The user who owns the file.
- **Group**: The group that the file belongs to.
- **Others**: All other users on the system.
  
## The Role of Hyphens (-) in Permissions Representation
Hyphens (-) in the permissions representation indicate the absence of a specific permission. For example:
- `r--` means Read permission is granted, but Write and Execute permissions are denied.
- `-wx` means Write and Execute permissions are granted, but Read permission is denied. 