# Creating Shared Folder and Mapping it to a Drive

### Objectives						

**Create and Map Share Folders**
 
- Create a main Share Folder called "AHTech Shared Folder" that is shared and can be accessed by the whole company.

- Within it, create a Share Folder for each department that can be accessed by only the members of their department. Each User should have their own home folder with modify permissions in their respective department. 

>**Note**: Users, Security Group (Department): Emily Walsh, Finance; Chris Chen,HR; Pedro Gonzales,Marketing.

- Ensure Only Emily Walsh has full modify permission to the Finance Folder along with her own homefolder. Chris Chen and Pedro Gonzales should only have fully modify permissions in their own home folder

- After verifying appropriate Access Control was given, Map "AHTech Shared Folder" to a network drive each New User's account for easy access.

## Creating a Shared Home Folder

To create a Shared Folder on the Domain Server, use the Server Manager software and under Shares, create a new Share Folder.
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

As a special note, Emily Walsh was given modified permission to the department folder. 

The other users, Chris Chen and Pedro Gonzales, only has modify permissions to their own home folders. 

<img src="Screenshots/Creating a Shared Folder/Emily_Walsh_Folder_NTFS_Permissions.PNG" alt="Special NTFS Permission" width="800">

Verifying Access Controls through user "Emily Walsh" in Finance Security Group. User should have access to Finance Folder, but not to any other department's folder.

<img src="Screenshots/Creating a Shared Folder/Access_Denied_From_Emily_Walsh_Account_To_Marketing_Folder.PNG" alt="Access Denied to Folder" width="800">

## Mapping Shared Folder to Drive

There are several ways to map a drive to a user's account. 
1) From the File Explorer through "This PC"
2) Creating a GPO (Group Policy Object) for all users on the Domain
3) Using `net use` command on CMD or Powershell 
4) From the User's properties profile tab in Active Directory


### Mapping a Network Drive through File Explorer

To map a drive from the File Explorer, `Right-Click` "This PC" and click "Map Network Drive". Then select a letter drive and folder to map the drive. Check "Reconnect at Sign-in" to have the drive mapped during every sign-in.

### Mapping a Network Drive through GPO

Here’s a polished, professional version of your paragraph:

To map a network drive using Group Policy, open the Group Policy Management Console `gpmc.msc` and create a new GPO with a descriptive name. Right-click the GPO and select Edit. 

Navigate to User Configuration > Preferences > Windows Settings > Drive Maps, and for each mapping, configure the following fields: Action: Create, Location: [Shared Folder Path], and Drive: [Select Drive Letter].

Run gpupdate /force in the command prompt to enforce Group Policy updates and ensure the policy is applied to all domain-joined devices.


### Mapping a Network Drive using CMD

To map a network drive via the command line, use the `net use` command followed by the desired drive letter and folder path. Include the `/persistent:yes` switch to ensure the drive is automatically reconnected each time the user signs in.

>**Note**: Ensure that the command prompt is run under the user’s account rather than as an administrator, as mapping the drive from an elevated session may prevent it from appearing correctly in the user’s session.

### Mapping a Network Drive through Active Directory in User Properties

To map a network drive via Active Directory, open the User Properties for the targeted account and navigate to the Profile tab. Under Home Folder, select Connect, choose the desired drive letter, and specify the folder path.
>**Note**: This only works if the user has full control permission of the folder







