# File-Screening-with-FSRM-on-Windows-Server
File Screening with FSRM on Windows Server

 **Overview**
This project demonstrates how to configure File Server Resource Manager (FSRM) on Windows Server to block specific file types (e.g.Mulitimedia Files) in shared folders using File Screening.

Tools & Requirements
Windows Server 2016/2019/2022/2025

FSRM Role installed

Admin rights

Shared folder to apply screen (e.g., D:\StaffFiles)

**Step-by-Step Configuration**
**Step-1**
Server Manager > Add Roles and Features
Select FSRM under File and Storage Services

**Step 2**: Open FSRM Console
Open Server Manager > Tools > File Server Resource Manager

**Step3** Create a File Screen Template**
Navigate to File Screening Management > File Screen Templates
Click Create File Screen Template
Name it: Block_Media_Files
Under File Groups, select:
Audio and Video Files
Or create a custom group (e.g., block .mp3, .mp4, .exe, etc.)
Under Screening Type, choose Active Screening
Optional: Configure email alerts or run a command/script
Save template

**Step 4: Apply File Screen to Folder**
Go to File Screens > Create File Screen
Select folder: e.g., D:\StaffFiles
Choose the Block_Media_Files template
Finish setup

**Step 5: Test the Block**
Try copying a .mp3 or .exe file to the folder
Windows will block the operation

