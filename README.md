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

- Windows Server 2025
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1-Create domain controller VM 
- Step 2-Create Client computer VM
- Step 3-Test connectivity between the two machines

<h2>Step 1</h2>

<p>
<img width="1886" height="849" alt="image" src="https://github.com/user-attachments/assets/2d9f98c2-4c2e-41fd-9d1b-9ead1a308b03" />
</p>
<p>
Created domain controller VM within Azure. Added it to the Active-Directory virtual network/subnet. 
</p>
<br />

<p>
<img width="1910" height="798" alt="image" src="https://github.com/user-attachments/assets/68e2bb13-1a9a-4b7b-8919-01373295f2e6" />

</p>
<p>
Changed DC-1's private IP address to staic on its NIC to prevent it from changing if DC-1 is shut off.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
