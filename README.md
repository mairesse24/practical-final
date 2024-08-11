# Configuring NTFS Permissions for DayGroup and NightGroup
## Introduction

As the IT administrator for a small corporate network, I am tasked with configuring the appropriate access permissions 
for two user groups, **DayGroup** and **NightGroup**, each group need access to specific folders.
This portfolio outlines the steps taken to configure these permissions, ensuring secure and appropriate access to the 
corresponding folders: `D:\Day Data` and `D:\Night Data`.

## Goals
1. Turn off permissions inheritance for each folder.
2. Convert existing permissions to explicit permissions.
3. Remove the Users group from each folder's Access Control List (ACL).
4. Add DayGroup to `D:\Day Data` and NightGroup to `D:\Night Data` and set appropriate permissions.

## Steps to Configure NTFS Permissions

### Step 1: Access D:\Day Data Folder Properties and Turn Off Permissions Inheritance

1. Open **File Explorer** and navigate to the D:\ drive. 
  ![file explorer](https://github.com/user-attachments/assets/80c8b467-37c6-4f95-8aac-e99de91bf7ec)

<a href="https://ibb.co/Gc977hd"><img src="https://i.ibb.co/hDcssqg/file-explorer.png" alt="file-explorer" border="0" /></a>

2. Right-click on the `Day Data` folder and select **Properties**, then navigate to the **Security** tab.
  ![DayData properties](https://github.com/user-attachments/assets/5afb94ea-fd68-42ee-bb1a-1631156cdc7e)
   The cursor is placed in the properties section.
  ![Data security prop](https://github.com/user-attachments/assets/d1abaa8a-e518-42a7-bdfa-3becda4cb06d)

3. Click on the **Advanced** button within the Security tab.
   ![daydata advance prop](https://github.com/user-attachments/assets/c7140689-2ba4-4e79-af46-dc2fd198297c)
4. In the Advanced Security Settings, select Disable inheritance.
     -This action ensures that the existing permissions are kept and allows you to be modify them explicitly.
   ![daydate inheritence](https://github.com/user-attachments/assets/aeb8bb96-122c-4953-9972-e808c7b8f6ac)
   
### Step 2: Removing the Users Group from the ACL and  Adding the Appropriate Group

1. In the **Permission Entries** section, find and select the **Users** group, then click on the **Remove** button. Confirm its removal by selecting "OK."
  ![remove users group](https://github.com/user-attachments/assets/7a4c4b3c-8e68-4830-b425-4e7e1122996f)
  After removing users group, DayData properties should look like this:
  ![after removing usergrp](https://github.com/user-attachments/assets/71cbf77e-08c1-4d59-81ad-eb27d94868de)

2. Click on **Edit** to introduce a new group to the ACL, then press "Add". 
  ![press add for new](https://github.com/user-attachments/assets/f7d125f0-20cf-4638-b7cd-8a0e8de156f5)

3. In the **Enter the object names to select**, enter DayGroup, then click **Check Names** to validate, and click OK
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

3. Click **Apply** and then **OK** to finalize the changes for this folder.
(This step ensures that your updates take effect and that the specified permissions are enforced.)
--------------------------------------

###  Set Permissions for the Night Data Folder
To set permissions for folder (`D:\Night Data` for NightGroup), repeat Steps 1 through 5, following the same process to set the appropriate permissions.

1. **Access the Folder Properties**:
   - Right-click on the `D:\Night Data` folder
   - Select "Properties."
   - Go to the "Security" tab and disable inheritance

2. **Remove and add NightGroup, and set it permissions**:
   - Select and remove "user".
   - Add NightGroup and grant it permissions by checking on "Full Control" under the allow column

Once doned setting permissions for Night Data, it should like this;
![Screenshot 2024-08-11 163705](https://github.com/user-attachments/assets/6a6e1528-ebd4-4ce9-8626-d7bd135340b6)

https://imgur.com/a/xN6r80P
<img src="https://i.imgur.com/xN6r80P.jpg" alt="Night Data Permissions" style="width: 50%; max-width: 600px;">


## Conclusion
By following these steps, I configured NTFS permissions for `D:\Day Data` and `D:\Night Data` folders. This configuration ensured that each group has the necessary access while enhancing the overall security of the corporate network. The implementation of explicit permissions and the removal of the Users group prevents unauthorized access, making a significant contribution to the security posture of the organization. 
