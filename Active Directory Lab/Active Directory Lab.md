# Active Directory Lab: OU, Group, User, and File Share Permissions

## 📌 Overview
This lab demonstrates the process of creating and managing Organizational Units (OUs), groups, users, and securing file shares with group-based permissions in an Active Directory environment.

---

## 🎯 Objectives
- Create an Organizational Unit (OU) in a domain.
- Create a security group and a user account within the OU.
- Assign the user to the group.
- Create a file share and grant permissions to the group.

---

## 🖥️ Lab Environment
- Windows Server (Domain Controller)
- Windows 10/11 Client (optional for testing access)
- Active Directory Users and Computers (ADUC)
- File Server role enabled

---

## 🛠️ Step-by-Step Process

### 1. Create a New Organizational Unit (OU)
1. On the lower-left open the Start menu, scroll down to **Windows Administrative tools** and choose **Active Directory Users and Computers**![[Pasted image 20250704140223.png]]
2. In the left pane, expand the **globomantics.co** domain near the top of the tree. 
3. Right-click **globomantics.co** and choose **New**, then **Organizational Unit**. ![[Pasted image 20250704140624.png]]
4. In the **New Object-Organizational Unit** window, enter the name *Globoticket* and click OK. This creates a new OU directly under the domain root.![[Pasted image 20250704140914.png]]
	1. It is always recommended to create a new top-level **OU** for new user objects, as you are not able to apply **Group Policy Objects** to the default **Computers and Users** containers, amoung other limitations. 
5. Expand **globomantics.co**, then right-click **Globoticket** and choose **New**, then **User**.![[Pasted image 20250704141640.png]]
	1. For the **First name**, enter Susan
	2. For the **Last name**, enter Smith
	3. For the **User logon name**, enter ssmith
	4. Click **Next**![[Pasted image 20250704141955.png]]
6. Enter Password1 in both the Password and Confirm password fields.
	1. In a production network, the password policy should normally be stricter, now allowing for simple passwords like this.
7. Click finish on the summary screen, then select **Globoticket**. You should see the newly-created user in the right-hand pane.![[Pasted image 20250704142408.png]]
8. Right-click on **Globoticket** and choose **New**, then **Group**.
9. Enter ```File Share Access``` for the Group name and click OK.![[Pasted image 20250704143136.png]]
10. Add the user **Susan Smith** to the group **File Share Access** using the following
	1. Double-click the File Share Access group
	2. Click on the **Members** tab
	3. Click **Add**... at the bottom of the **Members** box
	4. Enter the user ID **ssmith**  in the box labeled **Enter the object names to select** and click Check Names. The user ID should change to **Susan Smith \[ssmith@globomantics.co]**![[Pasted image 20250704144053.png]]
	5. Ensure that **Susan Smith** is listed in the **Members** box and click **OK**![[Pasted image 20250704144124.png]]
11. Click the folder icon on the taskbar to open the **File Explorer**
12. In the address bar at the top of the **File Explorer** window, enter \\\FS01![[Pasted image 20250704144437.png]]
13. A share named **FileShare** will appear, Double-click **FileShare**.
	1. FileShare was set-up ahead of time![[Pasted image 20250704145112.png]]
14. Right-click in the empty File Explorer pane and choose **New**, then **Folder**. Enter Shared Data for the folder name.
15. Right-click on Shared Data and choose **Properties**. 
16. Click on the **Security** tab, then click **Edit**...![[Pasted image 20250704145020.png]]
17. In the **Permissions for Shared Data** window, click **Add**... 
18. In the box labeled E**nter the object names to select**, enter **File Share Access**
19. Back at the **Permissions for Share Data** window, select the entry **File Share Access**, and check the box under **Allow** for **Full Control**![[Pasted image 20250704145453.png]]
20. Click **OK** on the **permissions for Shared Data** window, then **OK** on the **Shared Data Properties** window
