# Configuring Active Directory within Azure VMs #
<p align="center">
<img src="https://i.imgur.com/p3WJmAI.png" alt="osTicket logo"/>
</p>

<h1>Azure Active Directory - Prerequisites and Installation</h1>
This tutorial outlines setting up Azure Directory on a server and a Client that can remote in. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- STEP 1 - CREATING THE VIRTUAL MACHINES THROUGH AZURE
- STEP 2 - SETTING DC-1 TO A STATIC IP ADDRESS
- STEP 3 - TESTING CONNECTING FROM CLIENT1 TO DC-1
- STEP 4 - INSTALLING ACTIVE DIRECTORY
- STEP 5 - CREATE ADMIN AND NORMAL USER ACCOUNTS
- STEP 6 - JOIN CLIENT-1 TO DOMAIN
- STEP 7 - SETTING UP REMOTE DESTKOP FOR NON-ADMIN USERS ON CLIENT 1

<h2>Installation Steps</h2>

STEP 1 - CREATING THE VIRTUAL MACHINES THROUGH AZURE
<p>
<br />
I will use two virtual machines for this lab. The first one will be named “DC-1” which will be the server VM and the other will be named “Client-1”. See EXAMPLE 1A and 1B for designated settings on portal.azure.com. I also created login in credentials and recorded them for this lab (admin_user).
<p>
EXAMPLE 1A
<p>
<img src="https://i.imgur.com/kh9Qcgw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next web page you will input several items as shown in EXAMPLE 1B & 1C such as Resource Group, Virtual Machine etc. Ensure to have the inputs be the same as the example photo.
</p>
EXAMPLE 1B
<p>
<img src="https://i.imgur.com/t3Cuk3L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />
STEP 2 - SETTING DC-1 TO A STATIC IP ADDRESS
<br />
We select “DC-1”  and on it’s home screen select “Networking” on the left hand side (EXAMPLE 2A).
</p>
<br />
EXAMPLE 2A
<p>
<img src="https://i.imgur.com/LsCtO66.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once in the networking tab, we select “dc-1703” located to the right of Network Interface: (Example 2B)
</p>
<br />
EXAMPLE 2B
<p>
<img src="https://i.imgur.com/65iqYNy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then select “IP configurations” shown in EXAMPLE 2C.
</p>
<br />
EXAMPLE 2C
<p>
<img src="https://i.imgur.com/4NiCXGL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />
Then select “ipconfig1” which will lead to screen shown in EXAMPLE 2D. Here we select “Static” and we see that the private IP is “10.0.04”.
</p>
<br />
EXAMPLE 2D
<p>
<img src="https://i.imgur.com/F3nJQBi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 3 - TESTING CONNECTING FROM CLIENT1 TO DC-1
</p>
<br />
Logging remotely into DC-1 we will enable ICMPv4 traffic to be allowed in order to ping this DC-1 VM from Client-1 VM.
</p>
<br />
EXAMPLE 3A
<p>
<img src="https://i.imgur.com/WPGcYfb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
