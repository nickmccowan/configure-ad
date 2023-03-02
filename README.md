<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines: Domain controller-1 / Client-1)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory on Domain Controller-1
- Create an Admin and Normal User Account in Active Directory Domain Services
- Join Client-1 to your personalized domain i.e. mydomain.com
- Create additional users and log in to client-1 with one of the users info

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/K3eorGf.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Begin by setting up 2 virtual machines, one running Windows server 2022 (Domain Controller 1) the other running Windows 10 (Client 1). Set DC-1's NIC private IP address to static (shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/ohDahs0.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Login to DC-1 install Active Directory Domain Services, setup a new forest as 'mydomain.com' (can be anything)
</p>
<br />

<p>
<img src="https://i.imgur.com/PW0MmaF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Active Directory Users and Computers create new Organizational Units (_EMPLOYEES & _ADMINS). Create a new Employee 'Jane Doe', username: Jane_Admin
</p>
<br />

<p>
<img src="https://i.imgur.com/oY2DGhd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Add Jane_Admin to Domain Admins security Group.
</p>
<br />
<p>
<img src="https://i.imgur.com/Kk26Ord.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Login to client-1 and join it to the domain.
</p>
<br />
<p>
<img src="https://i.imgur.com/QQIjR8Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Allow Domain Users Access to Remote Desktop
</p>
<br />
<p>
<img src="https://i.imgur.com/8sHZeoE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Login to DC-1 using powershell run a script to create new Admin Accounts
</p>
<br />
