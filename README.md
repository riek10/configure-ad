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

- Enable ICMPv4 Connection
- Active Directory Installation
- Create Admin User
- Generate Random Users using Windows Powershell ISE

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/riek10/configure-ad/assets/113129662/7dc0ef21-ff1f-447d-81c0-ec3eb0ed2eab" height="80%" width="80%"/>
</p>
<p>
In step 1 , after creating the VMs necessary for this project i logged into both the Client-1 and DC-1 VMs to enable icmpv4 so the the two machines would be able to communicate with each other. After performing this step i tested the connection by running the "ping" command on Client-1 to verify the connection to the DC-1 VM.
</p>
<br />

<p>
<img src="https://github.com/riek10/configure-ad/assets/113129662/ee9a12d8-4a81-484d-9425-8e0e4ffd3dac" height="80%" width="80%"/>
</p>
<p>
Next I installed Active Directory on Domain Controller 1(DC-1). Active Directory is a database that connects users with different network resources used to get different tasks done. The database itself holds all user information and permissions permitted by the company.
</p>
<br />

<p>
<img src="https://github.com/riek10/configure-ad/assets/113129662/b07e546c-8c2c-4900-9631-fa199390cdf0" height="50%" width="50%"/>
<img src="https://github.com/riek10/configure-ad/assets/113129662/64551a2a-84d5-46c3-8b12-c84b430b6b99" heigt="50%" width="50%"/>
</p>
<p>
In step 3 i created an employee account that will serve as an admin user. Ill be adding this new user to the Domain Admins security group. 
</p>
<br />

<p>
  <img src="https://github.com/riek10/configure-ad/assets/113129662/dd1239d0-a250-4ea7-8385-02fedc319e7b" height="50%" width="50%"/>
  <img src="https://github.com/riek10/configure-ad/assets/113129662/835ceb3e-567f-420c-827f-5e195efc61d7" height="50%" width="50%"/>
</p>
<p>
  After successfuly logging in to the newly created Admin account i decided to use Windows Powershell ISE to randomly generate employees with both user & password credentials to verify successfuly logging on to the network with other users. Using the credentials "User:bob.taf & pass:Password1" i was able to successfuly login.
</p>
<br />
