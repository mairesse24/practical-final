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

### Step 1: Access D:\Day Data Folder Properties and Turn Off Permissions Inheritance

1. Open **File Explorer** and navigate to the D:\ drive. 
  ![file explorer](https://github.com/user-attachments/assets/80c8b467-37c6-4f95-8aac-e99de91bf7ec)
2. Right-click on the `Day Data` folder and select **Properties**, then navigate to the **Security** tab.
  ![DayData properties](https://github.com/user-attachments/assets/c1cbcc34-325c-4032-a071-f328f2109dd8)
   The cursor is placed in the properties section.
    ![Data security prop](https://github.com/user-attachments/assets/4aad66d9-322e-4c1d-b83e-00da30546619)
3. Click on the **Advanced** button within the Security tab.
   ![daydata advance prop](https://github.com/user-attachments/assets/c7140689-2ba4-4e79-af46-dc2fd198297c)
4. In the Advanced Security Settings, select Disable inheritance.
     -This action ensures that the existing permissions are retained but can now be modified explicitly.
or   (“This action keeps the current permissions but allows you to change them as needed.”)
   ![daydate inheritence](https://github.com/user-attachments/assets/aeb8bb96-122c-4953-9972-e808c7b8f6ac)
   
### Step 2: Removing the Users Group from the ACL and  Adding the Appropriate Group

1. In the **Permission Entries** section, find and select the **Users** group, then click on the **Remove** button. Confirm its removal by selecting "OK."
  ![remove users group](https://github.com/user-attachments/assets/7a4c4b3c-8e68-4830-b425-4e7e1122996f)
  After removing users group, DayData properties should look like this:
  ![after removing usergrp](https://github.com/user-attachments/assets/71cbf77e-08c1-4d59-81ad-eb27d94868de)

3. Click on **Edit** to introduce a new group to the ACL, then press "Add". 
  ![press add for new](https://github.com/user-attachments/assets/f7d125f0-20cf-4638-b7cd-8a0e8de156f5)

4. In the **Enter the object names to select**, enter DayGroup, then click **Check Names** to validate, and click OK
  ![check daygroup name](https://github.com/user-attachments/assets/2beba819-168f-4e4e-9c9f-045e72011964)
After adding DayGroup, it should look like this:
![after adding Daygrp](https://github.com/user-attachments/assets/d0c7a8de-1705-4ea7-9c73-3fca5a089517)

### Step 5: Assign Full Control Permissions

1. Select the new group that we just added "DayGroup". 
2. Below, in the "Permissions for DayGroup" section, in the "Allow" column, check **Full Control**. 
  ![chell full for daygrp](https://github.com/user-attachments/assets/6606d4fd-3285-4910-85eb-787c901e3e53)
now explain why check full
(Selecting "Full Control" grants users in the DayGroup comprehensive access to the folder, allowing them to read, write, modify, and delete files. This level of access is essential for effective folder management, particularly if the users need to update or manage the contents frequently.)
or
(Checking "Full Control" grants the group complete access to the folder, enabling them to read, write, modify, and delete files as needed. This is important for users who need comprehensive access to manage the contents of the folder effectively.)

4. Click **Apply** and then **OK** to finalize the changes for this folder.
(This step ensures that your updates take effect and that the specified permissions are enforced.)
--------------------------------------

###  Set Permissions for the Night Data Folder
To set permissions for folder (`D:\Night Data` for NightGroup), repeat Steps 1 through 5, followolling the same process to set the appropriate permissions.

1. **Access the Folder Properties**:
   - Right-click on the `D:\Night Data` folder
   - Select "Properties."
   - Go to the "Security" tab and disable inheritance

4. **Remove and add NightGroup, and set it permissions**:
   - Select and remove "user".
   - Add NightGroup and grant it permissions by checking on "Full Control" under the allow column

     
