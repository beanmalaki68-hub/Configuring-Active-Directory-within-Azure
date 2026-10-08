<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>

<h1>Preparing Active Directory infrastructure within Cloud (Azure)</h1>



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

# Step 1 - Creating a resoucre group and virtual network

The first thing I did was create a resource group in Microsoft Azure to organize and manage the resources for the virtual environment I was creating. Then, I created a virtual network for the two virtual machines to connect to. This virtual network provides the network infrastructure that allows the virtual machines to communicate with each other.

<h2> Step 1 Video Walkthorugh</h2>

https://youtu.be/ztGit00URzU

---

# Step 2 - Creating the Domain Controller 

I then created a Windows Server virtual machine that would be configured to act as the Domain Controller (DC) for the environment. The server would host Active Directory Domain Services (AD DS), which provides the services needed to manage users, computers, and other resources within the domain.

<h2>Step 2 Video Walkthrough</h2>

https://youtu.be/25Zd2apIPf0

---

# Step 3 - Creating a VM to act as a user in Active Directory 

Next, I created another virtual machine (VM) in Azure. This VM will be used as a client computer that I will join to the Active Directory domain and use as a user workstation in upcoming labs.


<h2>Step 3 Video Walkthrough</h2>

https://youtu.be/oO_7CMsn0I0

---

# Step 4 - Setting the Domain Controllers Private IP to Static 

After that, I configured the Domain Controller's IP address as static. I did this because I will be configuring the user VM to use the Domain Controller as its DNS server. The Domain Controller's IP address needs to remain consistent so that the user VM can reliably find and communicate with the correct DNS server.

<h2>Step 4 Video Walkthrough</h2>

https://youtu.be/KWmgiNGlb0k

---


# Step 5 - Logging into the Domain Controller and disabling the Firewall (for the lab)

I then logged into the Domain Controller and temporarily disabled the Windows Firewall. I did this so that the firewall would not interfere with network connectivity or block traffic while we test and configure the environment in the lab.

<h2>Step 5 Video Walkthrough</h2>


https://youtu.be/EcfDTyIQlb4

---


# Step 6 - Configuring the User VM to use the Domian Controller as the DNS server

Then, I configured the User VM's network settings to use the Domain Controller as its DNS server. I did this so that the User VM can use the Domain Controller's DNS service to locate and communicate with the Active Directory domain in our later labs.


<h2>Step 6 Video Walkthrough</h2>

https://youtu.be/aAMBOMso87s

---


# Step 7 - Testing connectivity 

I then logged into the User VM and pinged the Domain Controller to verify that the two virtual machines were able to communicate over the network. I also ran the ipconfig /all command to verify that the Domain Controller's IP address was configured as the User VM's DNS server.


<h2>Step 7 Video Walkthrough</h2>

https://youtu.be/8GIcbO44VBU

---
