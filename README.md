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
      <a href='https://postimg.cc/DJz20XbM'>
      <img src='https://i.postimg.cc/XJfX2KN4/file-explorer.png' alt='file-explorer' style="width: 70%; max-width: 900px;"/>
  </a>

2. Right-click on the `Day Data` folder and select **Properties**, then navigate to the **Security** tab.
   <a href='https://postimg.cc/zH5FTq86' target='_blank'>
      <img src='https://i.postimg.cc/BbP79vyS/Day-Data-properties.png' border='0' alt='Day Data Properties' style="width:               70%;  max-width: 700px;"/>
    </a>
    
   The cursor is placed in the properties section.
   
      <img src="https://i.postimg.cc/7LsyqfB0/Data-security-prop.png" alt="Data Security Prop" style="width: 680px; height:             400px;">

3. Click on the **Advanced** button within the Security tab.   
   <img src="https://i.postimg.cc/HsBzZXjw/daydata-advance-prop.png" alt="Daydata Advance Prop" style="width: 70%; height:       400px;">

4. In the Advanced Security Settings, select Disable inheritance and convert permissions from inherited to explicit.

   This action ensures that the existing permissions are kept and allows you to be modify them explicitly.
   <img src="https://i.postimg.cc/Njn4Yt6L/daydate-inheritence.png" alt="Daydate Inheritance" style="width: 60%; height:         400px;">
   
### Step 2: Removing the Users Group from the ACL and  Adding the Appropriate Group

1. In the **Permission Entries** section, find and select the **Users** group, then click on the **Remove** button. Confirm its removal by selecting **OK**.
  <img src="https://i.postimg.cc/2yHWwdT3/remove-users-group.png" alt="Remove Users Group" style="width: 700px; height: 400px;">

  After removing users group, DayData properties should look like this:
    <img src="https://i.postimg.cc/SK0MDxLL/after-removing-usergrp.png" alt="After Removing User Group" style="width: 50%; height: 400px;">

3. Click on **Edit** to introduce a new group to the ACL, then press **Add**. 
  <img src="https://i.postimg.cc/KjYkRkFb/press-add-for-new.png" alt="Press Add for New" style="width: 50%; height: 400px;">

4. In the **Enter the object names to select**, enter DayGroup, then click **Check Names** to validate, and click OK
  <img src="https://i.postimg.cc/T2k5B9q3/check-daygroup-name.png" alt="Check Daygroup Name" style="width: 600px; height: 300px;">

After adding DayGroup, it should look like this:

  <img src="https://i.postimg.cc/QxHKDT0k/after-adding-Daygrp.png" alt="After Adding Daygrp" style="width: 50%; height: 480px;">

### Step 5: Assign Full Control Permissions

1. Select the new group that we just added "DayGroup". 
2. Below, in the "Permissions for DayGroup"' section, in the "Allow" column, check **Full Control**. 
      <img src="https://i.postimg.cc/N0wKRPYp/check-full-for-daygrp.png" alt="Check Full for Daygrp" style="width: 50%; height: 485px;">

  Explaination: Checking **Full Control** grants the group complete access to the folder, enabling them to read, write,           modify, and delete files as needed.

4. Click **Apply** and then **OK** to finalize the changes for this folder.
(This step ensures that your updates take effect and that the specified permissions are enforced.)
--------------------------------------

###  Set Permissions for the Night Data Folder
To set permissions for folder (`D:\Night Data` for NightGroup), repeat Steps 1 through 5, following the same process to set the appropriate permissions.

1. **Access the Folder Properties**:
   - Right-click on the `D:\Night Data` folder
   - Select **Properties**.
   - Go to the **Security** tab and disable inheritance

2. **Remove and add NightGroup, and set it permissions**:
   - Select and remove **user**.
   - Add NightGroup and grant it permissions by checking on **Full Control** under the allow column

Once doned setting permissions for Night Data, it should like this;
<a href='https://postimages.org/' target='_blank'>
    <img src='https://i.postimg.cc/y8pR9TxG/Screenshot-2024-08-11-163705.png' style='width: 45%; max-width: 600px;' 
         border='0' alt='Screenshot-2024-08-11-163705'/>
</a>

## Conclusion
By following these steps, I configured NTFS permissions for `D:\Day Data` and `D:\Night Data` folders. This configuration ensured that each group has the necessary access while enhancing the overall security of the corporate network. The implementation of explicit permissions and the removal of the Users group prevents unauthorized access, making a significant contribution to the security posture of the organization. 



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Configuring NTFS Permissions</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4; /* Light grey background */
            color: #333; /* Dark text for readability */
        }
        h1 {
            background-color: #007BFF; /* Blue background for headings */
            color: white; /* White text on blue background */
            padding: 10px;
            border-radius: 5px;
        }
        h2, h3 {
            background-color: #e2e2e2; /* Light grey for subheadings */
            padding: 5px;
            border-radius: 4px;
        }
        section {
            background-color: white; /* White background for sections */
            padding: 20px;
            margin: 10px 0;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>

<h1>Configuring NTFS Permissions for DayGroup and NightGroup</h1>

<section>
    <h2>Introduction</h2>
    <p>As the IT administrator for a small corporate network...</p>
</section>

<section>
    <h2>Goals</h2>
    <ul>
        <li>Turn off permissions inheritance...</li>
        <li>Convert existing permissions...</li>
        <!-- Add more goals here -->
    </ul>
</section>

<section>
    <h2>Steps to Configure NTFS Permissions</h2>
    <h3>Step 1: Access D:\Day Data Folder Properties and Turn Off Permissions Inheritance</h3>
    <p>1. Open <b>File Explorer</b> and navigate to the D:\ drive.</p>
    <img src='https://i.postimg.cc/XJfX2KN4/file-explorer.png' alt='file-explorer' style="width: 70%; max-width: 900px;"/>
    <!-- Add additional steps and images -->
</section>

</body>
</html>





