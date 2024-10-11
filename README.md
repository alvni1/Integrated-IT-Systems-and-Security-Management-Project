<h1>Integrated IT Systems and Security Management Project</h1>



<h2>Description</h2>
Project consisted of: 
Setting up Windows, Kali Linux, and Windows Server 2019 virtual machine using VirtualBox, VMware Workstation Player, and cloud platform Azure
Configured secure remote access using SSH, Telnet, and Remote Desktop protocols with PuTTY and WinSCP
Set up and managed Azure Active Directory, configured IAM policies, and controlled access to cloud resources.
Established system monitoring with Windows Event Viewer and Linux syslog, applying security policies across both local and cloud-based VMs.
Configured network settings for VM communication


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 


<h2>Environments Used </h2>

- <b>Windows Server 2019</b> 
- <b>Kali Linux</b>
- <b>Microsoft Azure</b>
  
<h2>Program walk-through:</h2>
Here is all 3 of my VMs set-up and running. Kali Linux is running on VMware Workstation, while Windows Server 2019 is running on VM VirtualBox. Windows 11 is running on a VM within Microsoft Azure. 

![Screenshot (31)](https://github.com/user-attachments/assets/cf9bee11-982b-4b44-af06-34dd51d3b80a)

I configured my VM on Azure to be able to communicate with my other VMS by creating port rules. I created the AllowICMP rule for any port, as well as allowing incoming traffic on port 22 from my Kali Linux VM. 

![Screenshot (18)](https://github.com/user-attachments/assets/9adc20aa-1408-4a73-9b67-122d976cb048)

Here is all my VMs being able to pick up a ping from one another through pinging one another's IP address. 

![Screenshot from 2024-09-25 15-55-47](https://github.com/user-attachments/assets/dc1a13cc-ac76-4c90-9035-7aa445afc7e7)

![VirtualBox_DC_25_09_2024_16_21_46](https://github.com/user-attachments/assets/a258543b-a09a-4b81-916f-cd582ee970d7)

I used PuTTY to establish a SSH connection to my local Windows machine and Kali Linux VM.

![Screenshot (19)](https://github.com/user-attachments/assets/7a412797-df2a-485b-a0c2-13c27d62def0)

I used WinSCP to securely transfer files between my local machine and Kali Linux. 

![Screenshot (21)](https://github.com/user-attachments/assets/44c9c0bc-5735-4299-88ea-91370f67b165)
![Screenshot (20)](https://github.com/user-attachments/assets/28078535-213e-4e1b-9e52-f130655d4f96)

Here is an example of transferring a picture from my local machine to my Kali Linux VM. The picture is being displayed in the Kali Linux VM. 

![Screenshot (24)](https://github.com/user-attachments/assets/adf6f6f8-c1f9-4556-963c-686070052f1f)

![KALI LINUX-2024-09-25-15-14-49](https://github.com/user-attachments/assets/2e040fdd-1885-4b65-b778-90751dd2065e)

I used Entra ID with the cloud platform Azure to access the cloud-based identity access management and explore the different ways one can manage and secure identities. 

![Screenshot (25)](https://github.com/user-attachments/assets/5cdf13d1-e2a0-49a2-a027-aafca5db73a9)

I assigned the user alvni administrative roles, such as authentication administrator, meaning the user can edit and view authentication method information for any non-admin user. 

![Screenshot (27)](https://github.com/user-attachments/assets/e47de34c-d4e0-4234-8404-330cb4b98d0b)

The VM already had built-in authentication strengths for security purposes, but I added the following authentication strength: password and push notification. This would require users logging in to enter their password and have a push notification authentication. The push notification authentication would require the user to have another secure device that could receive and approve of the authentication alert.

![Screenshot (29)](https://github.com/user-attachments/assets/b5d663a6-7281-4934-ace5-ebc37bfaa794)


![Screenshot (30)](https://github.com/user-attachments/assets/7c26ffa1-06e9-42da-9ab6-bcdcc7e934dd)

I used Group Policy Management in the Windows Server VM in VirtualBOX to add user Lani Marie to the security filter, meaning any security policies created would apply to said user. 

![VirtualBox_DC_25_09_2024_15_27_24](https://github.com/user-attachments/assets/a412e692-49b7-49f3-8140-12df3803ca2f)
![VirtualBox_DC_25_09_2024_15_27_49](https://github.com/user-attachments/assets/fb8b5ee1-e99b-400a-9f93-f0a7711ed241)

I used Group Policy Management in the Windows Server VM in VirtualBOX to create password policies for the user Lani Marie. These policies ensure enhanced secueity so that it is not easy to hack into a user's account. Here you can see certain requirements, such as the maximum password age being 90 days, meaning the password would have to be changed every 90 days. 

![VirtualBox_DC_25_09_2024_16_08_58](https://github.com/user-attachments/assets/d2dcc17a-5ede-4135-b5c5-baeac2731042)

Here I used Powershell and the commmand "gpuupdate /force" to force any and all policies created to be effective immediately. 

![VirtualBox_DC_25_09_2024_16_09_56](https://github.com/user-attachments/assets/b7e9dc2b-5a49-4f42-8a7e-9e037c49e4e8)

I used Windows Event Viewer to access the system warning logs within my Windows Server VM. Here is all the warnings that have been logged into the system.

![VirtualBox_DC_25_09_2024_15_33_37](https://github.com/user-attachments/assets/a5e23f33-5351-4930-bd38-cb7e7f450baf)

I created a custom log folder that would specifically save all audit failures to it. By audit failures I mean any and all failed log-in attempts, as that could be an indication of a person trying to break into a user account to steal information or change network settings. 

![VirtualBox_DC_25_09_2024_15_36_00](https://github.com/user-attachments/assets/5d936611-1ea3-4838-a236-983868ce51c9)

I used the "sudo cat /var/log/syslog" command to access all logs on my Kali Linux VM. 

![KALI LINUX-2024-09-25-15-40-38](https://github.com/user-attachments/assets/7131a9c7-30d4-4f1d-9384-21b3391362aa)

In this commmand I used "tail -f" to access the last few files that have been logged and to continually watch the log file as new entries are added to the syslog. 

![KALI LINUX-2024-09-25-15-44-45](https://github.com/user-attachments/assets/c1bd8880-961a-4bc9-80e0-cd5786ce30d1)

![KALI LINUX-2024-09-25-15-46-38](https://github.com/user-attachments/assets/7d85dfb6-f048-44c1-8280-6dd70bcb267a)


![KALI LINUX-2024-09-25-15-47-33](https://github.com/user-attachments/assets/92eb23eb-2d3f-470a-bebb-0860eeb79068)
