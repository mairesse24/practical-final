# Configuring NTFS Permissions for DayGroup and NightGroup
## Introduction

As the IT administrator for a small corporate network, I was tasked with configuring the appropriate access permissions 
for two user groups, **DayGroup** and **NightGroup**, each requiring access to their specific folders located on the server.
This documentation outlines the steps taken to configure these permissions, ensuring secure and appropriate access to the 
corresponding folders: `D:\Day Data` and `D:\Night Data`.

## Goals

1. Turn off permissions inheritance for each folder.
2. Convert existing permissions to explicit permissions.
3. Remove the Users group from each folder's Access Control List (ACL).
4. Add DayGroup to `D:\Day Data` and NightGroup to `D:\Night Data` with appropriate permissions.
5. Assign Full Control to the respective group without altering other permissions.

## Steps to Configure NTFS Permissions
