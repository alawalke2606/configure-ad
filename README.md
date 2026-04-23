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
- Step 4-Install Active Directory
- Step 5-Create a Domain Admin user within the domain
- Step 6-Join Client-1 to domain (mydomain.com)
- Step 7-Setup Remote Desktop for non-administrative users on Client-1
- Step 8-Create a bunch of additional users and attempt to log into client-1 with one of the users


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
<img width="1059" height="789" alt="image" src="https://github.com/user-attachments/assets/cd8ee114-845a-48ae-a150-9902eebdac88" />
</p>
<p>
Disabled firewalls within DC-1 to test connectivity.
</p>
<br />

<h2>Step 2</h2>

<p>
<img width="1335" height="841" alt="image" src="https://github.com/user-attachments/assets/0d6c166f-b003-4b16-99d1-43386931d7b9" />
</p>
<p>
Created Client-1 VM within Azure. Added it to the Active-Directory virtual network/subnet.
</p>
<br />

<p>
<img width="752" height="723" alt="image" src="https://github.com/user-attachments/assets/468e094b-b418-4ef1-b927-456ec669a798" />
</p>
<p>
Set Client-1’s DNS settings to DC-1’s Private IP address
</p>
<br />

<p>
<img width="752" height="723" alt="image" src="https://github.com/user-attachments/assets/468e094b-b418-4ef1-b927-456ec669a798" />
</p>
<p>
Set Client-1’s DNS settings to DC-1’s Private IP address
</p>
<br />

<h2>Step 3</h2>

<p>
<img width="857" height="730" alt="image" src="https://github.com/user-attachments/assets/2b9fcaf9-88d8-44da-8bfd-5f38b1041266" />
</p>
<p>
Pinged DC-1's private IP address from Client-1 to ensure connectivity.
</p>
<br />

<p>
<img width="863" height="733" alt="image" src="https://github.com/user-attachments/assets/7c84b7e3-9bcb-4da7-933a-d93ce5791f81" />
</p>
<p>
Ran ipconfig /all on Client-1 to show that it is using DC-1 as the DNS server.
</p>
<br />

<h2>Step 4</h2>

<p>
<img width="787" height="565" alt="image" src="https://github.com/user-attachments/assets/8b3b6a03-7c51-42ea-8619-8ffd40abbcfc" />
</p>
<p>
Installed AD Domain Services on DC-1
</p>
<br />

<p>
<img width="776" height="571" alt="image" src="https://github.com/user-attachments/assets/af6a902f-8d23-4a5f-a27f-5d5ccb4d9311" />
</p>
<p>
Promoted DC-1 to a domain controller and created a new forest "mydomain.com."
</p>
<br />

<p>
<img width="1203" height="938" alt="image" src="https://github.com/user-attachments/assets/9799c5d4-1be5-44fd-b701-fc5028c82850" />
</p>
<p>
Logged in to DC-1 as a domain user.
</p>
<br />

<h2>Step 5</h2>

<p>
<img width="770" height="540" alt="image" src="https://github.com/user-attachments/assets/3815f015-a597-4520-bb0e-53663199587a" />
</p>
<p>
In Active Directory Users and Computers(AUDC), created two new Organizational Units(OU), _EMPLOYEES and _ADMINS.
</p>
<br />

<p>
<img width="1231" height="608" alt="image" src="https://github.com/user-attachments/assets/dcd1dcf4-328a-465b-bd23-0247758203e4" />
</p>
<p>
Created new employee called "Yoda Vader" and added the account to the Domain Admins security group.
</p>
<br />

<h2>Step 6</h2>

<p>
<img width="1231" height="608" alt="image" src="https://github.com/user-attachments/assets/dcd1dcf4-328a-465b-bd23-0247758203e4" />
</p>
<p>
Created new employee called "Yoda Vader" and added the account to the Domain Admins security group.
</p>
<br />




