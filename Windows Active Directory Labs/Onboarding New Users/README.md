# Onboarding New Users

## Objectives

1) Create the specified users in our branch in Los Angeles. Then create and assign them to their corresponding department security groups to ensure proper NTFS permission inheritance.

|Names		|Department	|Title				|Company Number		 |Email			|Notes							
|---------------|---------------|-------------------------------|------------------------|----------------------|-------------------------------------------------------|
|Emily Walsh	|Finance	|Chief Financial Officer (CFO)	|(382) 390-3905 Ext. 3945|`ewalsh@AHTech.com`	|Give special modify permission to the Finance Folder	|
|Chris Chen	|HR		|Talent Acquisition Specialist	|(382) 390-3905 Ext. 2034|`cchen@AHTech.com`	|Only give modify permission to their Home Folder	|						
|Pedro Gonzales	|Marketing	|Product Marketing Manager (PMM)|(382) 390-3905 Ext. 4902|`pgonzales@AHTech.com`|Only give modify permission to their Home Folder	|

Verify access to the new accounts before proceeding to creating new share folders.						


2) **Create Share Folders**
 
- Create a main Share Folder called "AHTech Shared Folder" that is shared and can be accessed by the whole company.
- Within it, create a Share Folder for each department that can be accessed by only the members of their department. Each New User should have their own home folder with modify permissions in their respective department. 

3) Map "AHTech Shared Folder" to a drive each New User's account for easy access.

## Onboarding Process

### Creating New Users

In the Los Angeles/Users OU, create the New User and their credentials. Then create a password and tick the necessary options for the new account. 
>**Note**: "Emily Walsh" and a Windows 11 Client will be used as an example throughout the process. This will be the same for the other New Users and on Windows 10 Client. 

<img src="Screenshots/Creating New Users and Security Groups/Emily_Walsh_New_User.PNG" alt="Creating New Users" width="800">

<img src="Screenshots/Creating New Users and Security Groups/Emily_Walsh_New_User_Password.PNG" alt="New User Password Creation" width="800">

In the same `Properties` dialog box under the `General` and `Organization` Tab, add in other information and descriptions for each end user.

<img src="Screenshots/Creating New Users and Security Groups/Emily_Walsh_General_Informations.PNG" alt="General Tab" width="800">

<img src="Screenshots/Creating New Users and Security Groups/Emily_Walsh_Organization_Informations.PNG" alt="Organization Tab" width="800">

Finally verify access to the new account by logging into a domain client.

<img src="Screenshots/Creating New Users and Security Groups/Emily_Walsh_Login_Confirmation.PNG" alt="Login Confirmation" width="800">

### Creating Security Groups

Similar to Users, Active Directory allows creation of Security Groups to easily manage and set group policies for Users in each department.

**Understanding Group Scopes**
|Group Scopes	|Users		|Resources	|Common Use		|
|---------------|---------------|---------------|-----------------------|
|Domain Local	|Any Domain	|Same Domain	|Managing Permissions	|
|Global		|Same Domain	|Any Domain	|Managing Roles		|
|Universal	|Any Domain	|Any Domain	|Enterprise Roles	|

**Understanding Group Types**

|Group Types	|Common Use			|
|---------------|-------------------------------|
|Security	|Managing Access Control	|
|Distribution	|Managing Email Distribution	|

For the objective, we will be using `Global` Group Scope and `Security` Group Type for our Security Group Departments

<img src="Screenshots/Creating New Users and Security Groups/Finance_Group_Creation.PNG" alt="Creating Security Groups" width="800">

**Adding Members to Security Groups**

To add a member to a security group, `right-click` the Security group and click `Properties`. Under the `Members`tab enter the members name and add them to the group.

<img src="Screenshots/Creating New Users and Security Groups/Finance_Group_Adding Members.PNG" alt="Adding Members to Security Groups" width="800">

## Creating a Shared Home Folder

To create a Shared Folder on the Domain, use the Server Manager under Shares to create a new Share Folder.
The folder was named "AHTech Shared Folder" as directed by the objective.

<img src="Screenshots/Creating a Shared Folder/Creating_A_New_Share_Folder.PNG" alt="Creating a New Share Folder" width="800">

<img src="Screenshots/Creating a Shared Folder/Naming_NewShareFile.PNG" alt="Naming New Share Folder" width="800">

After the Server's Main Shared Folder is created, each department's designated shared folder can be created (Finance, HR, and Marketing).

<img src="Screenshots/Creating a Shared Folder/Create_Share_Folder_For_Each_Department.PNG" alt="Designated Department Shared Folder" width="800">

Before Sharing the Folder, we must ensure that each Shared Folder has the correct Sharing and NTFS permissions using the "Least Priviledge" princicple.
For best practice it is best to share the folder using only `Advanced Sharing` and give "Full Control" to Everyone or specific group. Then fine tune the Access Control with NTFS Permissions.

<img src="Screenshots/Creating a Shared Folder/AHTech_Shared Folder_Sharing_Permission.PNG" alt="Advanced Sharing Permissions" width="800">

<img src="Screenshots/Creating a Shared Folder/AHTech Shared Folder_NTFS_Permissions.PNG" alt="Main Shared Folder NTFS Permissions" width="800">

In this objective, Everyone has accessed to the Shared Folder, "AHTech Shared Folder", but NTFS Permissions only allows each Security Group access to their respective department's shared folder, but denied access to other department's shared folders.

<img src="Screenshots/Creating a Shared Folder/Create_Share_Folder_For_Each_Department.PNG" alt="Department Share Folder Creation" width="800">

<img src="Screenshots/Creating a Shared Folder/Finance_Folder_NTFS_Permissions.PNG" alt="Finance Folder NTFS Permissions" width="800">

<img src="Screenshots/Creating a Shared Folder/Marketing_Folder_NTFS_Permissions.PNG" alt="Marketing Folder NTFS Permissions" width="800">

As a special note, Emily Walsh was given modified permission to the department folder. The other users, Chris Chen and Pedro Gonzales, only has modify permissions to their own home folders. 

<img src="Screenshots/Creating a Shared Folder/Emily_Walsh_Folder_NTFS_Permissions.PNG" alt="Special NTFS Permission" width="800">

Verifying Access Controls through user "Emily Walsh" in Finance Security Group. User should have access to Finance Folder, but not to any other department's folder.

<img src="Screenshots/Creating a Shared Folder/Access_Denied_From_Emily_Walsh_Account_To_Marketing_Folder.PNG" alt="Access Denied to Folder" width="800">

## Mapping Shared Folder to Drive






