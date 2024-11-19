# Configuring Windows File Permissions with Active Directory & Powershell
The contents below include documentation of creating a folder structure, Active Directory security groups and configuring Windows File Permissions from the Windows UI and then from Powershell.

# First Folder Structure (Windows UI)
The Departments folder would lead into the departments of the school along with the subfolders within each department

<img width="459" alt="image" src="https://github.com/user-attachments/assets/3f629b1f-67c3-4747-8fc2-65373307cc78">

# Created the Folder Structure in the Windows UI
The folder structure below was implemented into a new folder that I created to store the three main folders. 

<img width="464" alt="image" src="https://github.com/user-attachments/assets/1ae2874b-407a-4a5f-8e5d-c6e55134f3a8">


Each folder (Networking, Security & Programming) contained two subfolders (class names) that stored three subfolders within them. (Each class contained the same subfolders being assignments, faculty notes and lecture notes)

<img width="466" alt="image" src="https://github.com/user-attachments/assets/73c91caf-261b-44e4-8595-a96c0c271b1b">

# Created Active Directory Security Groups in the Windows UI
Security groups were created using Active Directory Users and Computers for both students and faculty with the faculty group

<img width="468" alt="image" src="https://github.com/user-attachments/assets/df0341d9-4c40-4641-b015-04ad4aa292cc">


# Configuring Permissions in the Windows UI
The faculty group was granted full control access over the current folder, its subfolders and files while those in the student group were only given read & execute access to the same materials. To perform this, I used Advanced Security Settings for the “PRO202” class folder, disabled inheritance so that the PRO202 folder didn’t inherit permissions from its parent folders, added the groups I created by clicking add and modifying the permissions using the checkboxes for basic permissions. (*Granular permissions could have been added by clicking “Show Advanced Permissions” in the top right-hand corner of the permissions screen*)

<img width="467" alt="image" src="https://github.com/user-attachments/assets/62ba5bad-5f93-4ca7-b0d0-4bd4c2e24394">

The “SEC202” class folder with the groups having the same access as they did in the “PRO202” folder, respectively.

<img width="463" alt="image" src="https://github.com/user-attachments/assets/7711d071-03f1-4a38-8242-62e0cdbb5b15">

# Second Folder Structure (Powershell)
The Departments folder would lead into the departments of the school along with the subfolders within each department. (*Different classes were used as subfolders in comparison to using only File Explorer in the UI*)

<img width="451" alt="image" src="https://github.com/user-attachments/assets/143bc22c-3864-400f-a152-52a701ea67a9">

# Created the Folder Structure Using Powershell
The folder structure was implemented in PowerShell by using commands such as mkdir and cd. After implementation, the entire layout of the structure can be seen in PowerShell using the tree command.

<img width="463" alt="image" src="https://github.com/user-attachments/assets/1284a8b7-d97b-4c21-9894-3448fb7ec0cd">

# Created Active Directory Security Groups Using Powershell
Created faculty and student security groups in PowerShell using commands such as “New-ADGroup”, “ForEach-Object {Add -**}” and “Get-ADUser”. The “Get-ADGroupMember” command was run to display the members of each group.

<img width="460" alt="image" src="https://github.com/user-attachments/assets/77569d13-ebb1-404b-a0f4-74273cd21e19">

# Configuring Permissions Using Powershell
The figure below displays the granting and removal of permissions based on group type for the Networking, NET303 and NET404 folders in PowerShell using the “icacls” command.

<img width="466" alt="image" src="https://github.com/user-attachments/assets/193e9656-6610-4819-af8f-f4bf783424e4">

The results of the permissions added and granted in PowerShell can also be seen here in the Advanced Security Settings for the NET404 folder.

<img width="462" alt="image" src="https://github.com/user-attachments/assets/9372d573-0f2b-4759-8211-79fd747650c3">
