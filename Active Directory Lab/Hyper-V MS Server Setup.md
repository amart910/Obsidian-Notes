- This tutorial is for enabling Hyper-V and setting up a MS server VM to practice using Active Directory
1. Go to the start menu and search for Turn Windows features on or off
	1. ![Pasted image 20250708172720](../Networking%20and%20Security/Images/Pasted%20image%2020250708172720.png)
2. Enable Hyper-V in Windows Features and click OK.
	1.![Pasted image 20250708173013](../Networking%20and%20Security/Images/Pasted%20image%2020250708173013.png)
	1.  When prompted, click on reboot 
3. Go to start menu and search for Hyper-V Manager and run it
4. To create a new virtual machine (VM), click on NEW under the Actions Tab
	1. Then click on Virtual Machine
	2. This will start the New Virtual Machine Wizard, click Next if it starts in Before You Begin
	3. You can rename the VM in the Specify Name and Location section
	4. In the Specify Generation section, click on Generation 1.
		1. Gen 1 is more compatible to older versions of MS server or 32 bit guest OSs
	5. In the next section, assign 2048 MB of memory
	6. Configure Networking connection with Default Switch
	7. Create a Virtual Hard Disk