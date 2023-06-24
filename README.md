# Configuring-Active-Directory-within-Azure-VMs
<p align="center">
<img src="https://i.imgur.com/p3WJmAI.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- STEP 1 - CREATING THE VIRTUAL MACHINE THROUGH AZURE
- STEP 2 - SETTING DC-1 TO A STATIC IP ADDRESS
- STEP 3 - TESTING CONNECTING FROM CLIENT1 TO DC-1
- STEP 4 - INSTALLING ACTIVE DIRECTORY
- STEP 5 - CREATE ADMIN AND NORMAL USER ACCOUNTS
- STEP 6 - JOIN CLIENT-1 TO DOMAIN
- STEP 7 - SETTING UP REMOTE DESTKOP FOR NON-ADMIN USERS ON CLIENT 1

<h2>Installation Steps</h2>

STEP 1 – Creating Virtual Machine Through Azure
<p>
Go to portal.azure.com to set up a VM (you can create a free account with $200 credit here https://azure.microsoft.com/en-us/free/). 
<p>
EXAMPLE 1A
<p>
<img src="https://i.imgur.com/PowGPR4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next web page you will input several items as shown in EXAMPLE 1B & 1C such as Resource Group, Virtual Machine etc. Ensure to have the inputs be the same as the example photo.
</p>
EXAMPLE 1B
<p>
<img src="https://i.imgur.com/ShRYyCV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />
For the “Administrator account” section ensure to create username and password credentials that will be required on future steps.
</p>
<br />
EXAMPLE 1C
<p>
<img src="https://i.imgur.com/cdiXyVD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then select “Networking” at the top of the page and make sure the inputs match EXAMPLE 1D then select “Review and Create”.
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
line
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
line
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
line
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
line
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
line
</p>
<br />
EXAMPLE 1D
<p>
<img src="https://i.imgur.com/jzxbosV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
