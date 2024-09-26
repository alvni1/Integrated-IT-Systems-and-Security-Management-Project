<h1>Integrated IT Systems and Security Management Project</h1>



<h2>Description</h2>
Project consisted of: 
Set up Windows, Kali Linux, and Windows Server 2019 virtual machine using VirtualBox, VMware Workstation Player, and cloud platform Azure
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
Here is all 3 of my VMs set-up and running.

![Screenshot (31)](https://github.com/user-attachments/assets/cf9bee11-982b-4b44-af06-34dd51d3b80a)

I configured my VM on Azure to be able to communicate with my other VMS by creating port rules. 

![Screenshot (18)](https://github.com/user-attachments/assets/9adc20aa-1408-4a73-9b67-122d976cb048)

Here is all my VMs being able to pick up a ping from one another.

![Screenshot from 2024-09-25 15-55-47](https://github.com/user-attachments/assets/dc1a13cc-ac76-4c90-9035-7aa445afc7e7)

![VirtualBox_DC_25_09_2024_16_21_46](https://github.com/user-attachments/assets/a258543b-a09a-4b81-916f-cd582ee970d7)

I used PuTTY to establish a SSH connection to my Windows and Kali Linux VM.

![Screenshot (19)](https://github.com/user-attachments/assets/7a412797-df2a-485b-a0c2-13c27d62def0)

I used WinSCP to securely transfer files between my local machine and Kali Linux. 

![Screenshot (21)](https://github.com/user-attachments/assets/44c9c0bc-5735-4299-88ea-91370f67b165)
![Screenshot (20)](https://github.com/user-attachments/assets/28078535-213e-4e1b-9e52-f130655d4f96)

![Screenshot (24)](https://github.com/user-attachments/assets/adf6f6f8-c1f9-4556-963c-686070052f1f)

![KALI LINUX-2024-09-25-15-14-49](https://github.com/user-attachments/assets/2e040fdd-1885-4b65-b778-90751dd2065e)

Entra ID 

![Screenshot (25)](https://github.com/user-attachments/assets/5cdf13d1-e2a0-49a2-a027-aafca5db73a9)

![Screenshot (27)](https://github.com/user-attachments/assets/e47de34c-d4e0-4234-8404-330cb4b98d0b)
![Screenshot (29)](https://github.com/user-attachments/assets/b5d663a6-7281-4934-ace5-ebc37bfaa794)
![Screenshot (30)](https://github.com/user-attachments/assets/7c26ffa1-06e9-42da-9ab6-bcdcc7e934dd)

Using Group Policy Management to create password policies. 

![VirtualBox_DC_25_09_2024_15_27_24](https://github.com/user-attachments/assets/a412e692-49b7-49f3-8140-12df3803ca2f)
![VirtualBox_DC_25_09_2024_15_27_49](https://github.com/user-attachments/assets/fb8b5ee1-e99b-400a-9f93-f0a7711ed241)

![VirtualBox_DC_25_09_2024_16_08_58](https://github.com/user-attachments/assets/d2dcc17a-5ede-4135-b5c5-baeac2731042)

![VirtualBox_DC_25_09_2024_16_09_56](https://github.com/user-attachments/assets/b7e9dc2b-5a49-4f42-8a7e-9e037c49e4e8)

Using syslog and windows event viewer to create log folders 

![VirtualBox_DC_25_09_2024_15_36_00](https://github.com/user-attachments/assets/5d936611-1ea3-4838-a236-983868ce51c9)

![VirtualBox_DC_25_09_2024_15_33_37](https://github.com/user-attachments/assets/a5e23f33-5351-4930-bd38-cb7e7f450baf)
