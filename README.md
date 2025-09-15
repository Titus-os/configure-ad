<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a Resource Group, Virtual Network, and VMs (DC-1 and Client-1) with DC-1’s NIC Set to Static IP and Client-1’s DNS Set to DC-1’s Private IP  
- Install Active Directory Domain Services on DC-1 and Promote It as a Domain Controller for mydomain.com  
- Join Client-1 to the mydomain.com Domain and Verify in ADUC
- Configure Group Policy for Account Lockout Threshold (5 Attempts) and Observe Account Lockout 

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Creating a resource group, a virtual network (VNet), and two VMs (DC-1 as Windows Server 2022 and Client-1 as Windows 10) in the same VNet/subnet, setting DC-1’s NIC to a static private IP, and configuring Client-1’s DNS to DC-1’s private IP is critical. This establishes the Azure infrastructure for the AD environment, ensuring stable communication between the domain controller (DC) and client, with DNS settings enabling domain joining and AD functionality.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Installing Active Directory Domain Services (AD DS) on DC-1 and promoting it as a domain controller for a new forest (mydomain.com) is essential. This step sets up the core AD environment, enabling centralized user and computer management, authentication, and policy enforcement, which are the backbone of the lab’s objectives.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Group Policy to set an account lockout threshold of 5 failed login attempts, attempting to log in 6 times with a bad password, and observing the lockout in AD is vital. This step demonstrates AD’s security capabilities, showing how policies enforce account protection and how administrators manage lockouts, a common real-world scenario.


</p>
<br />
