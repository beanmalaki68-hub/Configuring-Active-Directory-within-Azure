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
<img width="1857" height="916" alt="image" src="https://github.com/user-attachments/assets/04a68180-d9d8-431c-8fac-f71057f9b47a" />


</p>

- The first step is to create a Resource Group in Azure.
- A Resource Group provides a logical container for the Azure resources used in this lab.
- I created a new Resource Group in Microsoft Azure that will contain the resources used for the Active Directory infrastructure.
- Resource Groups make it easier to organize, manage, monitor, and eventually remove related Azure resources.

<br />

<p>
<img width="1221" height="808" alt="image" src="https://github.com/user-attachments/assets/07b52556-1a6f-4b71-8330-7309a9c60754" />

</p>

- Next I created a Virtual Network and Subnet 
- I created a Virtual Network and configured a subnet for the lab's virtual machines.
- A Virtual Network provides the private networking environment that allows Azure resources to communicate with one another.
- For an Active Directory environment, reliable network communication between the Domain Controller and clients is essential.

<br />

<p>
<img width="1842" height="912" alt="image" src="https://github.com/user-attachments/assets/76142737-7ea8-412f-8777-1c6e27994b43" />

</p>


- The next step is to create the first virtual machine.
- I created a Windows Server 2025 virtual machine named DC-1(Domain Controller).
- A Domain Controller is responsible for providing centralized identity and authentication services within an Active Directory domain.

<br />

<p>
  <img width="1802" height="911" alt="image" src="https://github.com/user-attachments/assets/7a96633d-82f3-4be8-9c69-1e4c9c69ba6c" />

</p>

- The next step is to create the client computer that will eventually communicate with the Domain Controller.
- I created a Windows 11 virtual machine named Client-1.
- Client-1 will represent a workstation that communicates with the Active Directory infrastructure hosted by DC-1.

<p>
  <img width="693" height="852" alt="image" src="https://github.com/user-attachments/assets/1fef9f7f-413b-4a7f-b1b4-ace98052ee91" />

</p>

- After creating DC-1, configure its Network Interface Card (NIC) so that its private IP address is static.
- I configured the private IP address assigned to DC-1 as static through Azure.
- A Domain Controller needs a predictable network address.
- Client computers will eventually need to know where to find services provided by the Domain Controller, including DNS and Active Directory services.

  
<p>
  <img width="1292" height="959" alt="image" src="https://github.com/user-attachments/assets/759f8735-6928-4391-8d2f-d378cb76f703" />

</p>

- Next I logged into DC-1 and disabled the Windows Firewall for lab testing
- I logged into the Windows Server 2025 virtual machine using Remote Desktop.
- This allows the lab to isolate basic network connectivity problems while testing communication between DC-1 and Client-1.

  Security Note: Disabling a firewall is not recommended for a production system. This is being done specifically because the provided lab checklist calls for it during connectivity testing.

<p>
  <img width="1140" height="552" alt="image" src="https://github.com/user-attachments/assets/ff5b631e-7e02-46b8-9c74-a796bf63cb4b" />

</p>

- The next step would be to make sure that client-1 DNS it is pointing at the DC-1.
- I configured the DNS settings on Client-1 so that the preferred DNS server is the private IP address assigned to DC-1.
- Active Directory relies heavily on DNS to locate domain services. Configuring the client to use the Domain Controller as its DNS server prepares the workstation for future domain-related labs.

  
