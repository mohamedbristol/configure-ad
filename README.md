<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1- Creating virtual machine
- Step 2- Ping DC-1's IP address
- Step 3- Enabling imbound rules via DC-1
- Step 4- Configuring users and allowing to logon to Client-1's OS
- Step 5- Restting a password

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/f7mtfnc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here in order to start the lab I must first create a virtual machine, here it is Windows Server 2022 imaginer. I also created another virtual machines called "Client-1" with a windows 10 imaginer so i can connect it to the domain controller later in this lab.
</p>
<br />

<p>
<img src="https://i.imgur.com/u6W5FSw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As illstrauted above, im trying to ping my DC-1's IP address via my Client-1's operating system on command prompt. It timed out and I wasn's able to get any request by I am going to configure to see if I can eventually ping DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/zHHNMQG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It started to ping DC-1's IP address now because I enabled two rule on DC-1 via mircosoft firewall which where ICMPv4 echco rules.Once I enabled it, the requests started to come in and the ping was successful!
</p>
<br />

<p>
<img src="https://i.imgur.com/qjNtZmt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I am remote connecting into an account that was created by me from configuring a countless amount of domain users by allowing them to log in remotely to Client-1's virtual machine. Now essentially "bac.dap" is on the domain which allows "bac.dap" and all the other to sign on to Client-1's OS even if it's their first time on it.
</p>
<br />

<p>
<img src="https://i.imgur.com/XO9ksrz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I purposely tried to lock out an account so I could practice and try to reset the password and unlock the account for the user in active directory.
</p>
<br />
