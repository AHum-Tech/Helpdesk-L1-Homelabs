# Onboarding and Offboarding Users

### Objectives

**Onboarding**
Create the specified users in our branch in Los Angeles. Then create and assign them to their corresponding department security groups to ensure proper NTFS permission inheritance.

|Names		|Department	|Title				|Company Number		 |Email			|							
|---------------|---------------|-------------------------------|------------------------|----------------------|
|Emily Walsh	|Finance	|Chief Financial Officer (CFO)	|(382) 390-3905 Ext. 3945|`ewalsh@AHTech.com`	|
|Chris Chen	|HR		|Talent Acquisition Specialist	|(382) 390-3905 Ext. 2034|`cchen@AHTech.com`	|						
|Pedro Gonzales	|Marketing	|Product Marketing Manager (PMM)|(382) 390-3905 Ext. 4902|`pgonzales@AHTech.com`|

Verify access to the new accounts.

**Offboarding**
						

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

### Setting Up New User in Microsoft 365 

**Creating Email Account**







