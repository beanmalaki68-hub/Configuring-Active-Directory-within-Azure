<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This lab focuses on preparing the infrastructure needed for an Active Directory (AD) environment in Microsoft Azure. The lab begins by creating an Azure Resource Group, Virtual Network, and subnet. A Windows Server 2025 virtual machine is then created to serve as the Domain Controller (DC-1).

A second virtual machine, Client-1, is created on the same Virtual Network. Client-1 is configured to use the private Internet Protocol (IP) address of DC-1 for Domain Name System (DNS) resolution. Connectivity between the two virtual machines is then tested using ping and ipconfig /all.
.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 Pro (25H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Deploy the Azure Network Infrastructure
- Deploy and Configure the Domain Controller
- Deploy the Client VM
- Configure Client DNS and Connectivity
- Verify the Network Configuration

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1852" height="915" alt="image" src="https://github.com/user-attachments/assets/4237adf8-11cd-427d-99b6-a10160a24340" />

</p>

- The first step is to create a Resource Group in Azure.
- A Resource Group provides a logical container for the Azure resources used in this lab.
- I created a new Resource Group in Microsoft Azure that will contain the resources used for the Active Directory infrastructure.
- Resource Groups make it easier to organize, manage, monitor, and eventually remove related Azure resources.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
