# Creating Group Policies

### Objective

Create a GPO for each of the following:

+ Password Length and Expiration

+ Specify a Desktop Wallpaper for all Users

+ Control Panel Access Restrictions

+ Deny Removable Drive from being Accessed

+ Account Lockout Policy 


## Understanding Group Policies and How to Create One

### Understanding Group Policies

Group Policies are divided into two main types of configurations: "Computer Configurations" and "User Configurations." Each of these categories includes both "Policies" and "Preferences," which contain predefined settings that can be applied throughout the domain.

**Computer Configurations**
Settings and Policies pertaining to the computer regardless of the user who logs in. They control aspects such as software installation, security settings, and Operating System functionalities.

**User Configurations**
Settings targetting user accounts and their environments. These settings apply when a user logs into any computer within a domain, allowing for personalized environments, such as desktop settings, application configurations, and user permissions.

**Policies**
Mandatory settings that cannot be overidden by users and takes effect immediately upon application.

**Preferences**
Optional settings that users can modify and change as needed.

### How to Create Group Policies

To create a group policy, open Group Policy Management, or `gpmc.msc` on command line interface. 

Righ-click the Domain that you want the GPO to apply to and select "Create a GPO in this domain, and Link it here..."

<img src="Screenshots/1_Creating_GPO.PNG" alt="Creating GPO" width="800">

Name the GPO. For organization, it's best to name it after its function.

Once the GPO has been created, edit the GPO and set the settings for the Group Policy.


## Password Length and Expiration GPO

Password Policy can be set under: `Computer Configurations` > `Policies` > `Windows Settings` > `Security Settings` > `Account Policies` > `Password Policy` 

<img src="Screenshots/2_Password_Policy_Directory_Navigation.PNG" alt="Password Policy Directory Navigation" width="800">

<img src="Screenshots/3_Password_Policy_Editting_Settings.PNG" alt="Password Policy Settings Edit" width="800">

## Specify a Desktop Wallpaper for all Users

Desktop Wallpaper Group Policy Settings can be found under: `User Configurations` > `Policies` > `Administrative Template` > `Desktop` > `Desktop` > `Desktop Wallpaper`

<img src="Screenshots/4_Desktop_Wallpaper_Directory_Navigation.PNG" alt="Desktop Wallpaper Directory Navigation" width="800">

<img src="Screenshots/5_Desktop_Wallpaper_GPO_Setting.PNG" alt="Desktop Wallpaper GPO Setting" width="800">

## Control Panel Access Restrictions



