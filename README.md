# configure-ad-part-1
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in Azure (Part One)</h1>
This is part one of a tutorial that outlines the implementation of on-premises Active Directory within Azure Virtual Machines. In this segment, I'll start by creating a subscription account and two virtual machines in Azure that I'll be using for my lab. One will be Windows Server 2022, and the other will be Windows 10. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 

<h2>Deployment and Configuration Steps</h2>

- Step 1: Create Subscription and Resource Group
- Step 2: Choose Virtual Machines  
- Step 3: Configure Basic Settings
- Step 4: Access Virtual Machines using Remote Desktop Protocol

<h2>Step 1: Create Subscription and Resource Group</h2>

<p>
<img src="https://i.imgur.com/vCSqzgJ.png" height="80%" width="80%" alt="Resource Group"/>
</p>
<p>
The first step is to sign up for Azure and create a subscription. Once that's done, I will create a resource group. A resource group is a container that helps to organize all of the resources for the virtual machines I will create in the next step. To create a resource group, navigate to the Azure portal, select "Resource groups" from the left-hand menu, and click on "Create resource group." Then, I will provide a memorable name (ADLab), and choose a region (East US) for my resource group.
</p>

<p>
<img src="https://i.imgur.com/5sqozy9.png" height="80%" width="80%" alt="Resource Group"/>
</p>

<br />

<h2>Step 2: Choose Virtual Machines</h2>

<p>
<img src="https://i.imgur.com/vzT7Icu.png" height="80%" width="80%" alt="Virtual Machines"/>
</p>
<p>
I will then proceed to create my first virtual machine, Windows Server 2022, by selecting "Create a resource" from the Azure portal, and choosing "Virtual machines". I will name this first virtual machine "DC-1", because I will be installing Active Directory Domain Services onto the server, and turning it into a domain controller. The next virtual machine I will create afterward is a Windows 10 machine called "Client-1" because it's going to be joined to the domain (DC-1). I will also choose a memorable username (labuser), and password for both virtual machines. </p>
<br />

<h2>Step 3: Configure Basic Settings</h2>

<p>
The important part is to make sure that both virtual machines are on the same VNet (Virtual Network, and the same resource group (ADLab) before deploying. After deploying DC-1, it's best to wait a few minutes before deploying Client-1 to allow DC-1 to have time to create all its resources. This will ensure that both virtual machines will end up on the same VNet and not on two separate VNets. </p>
</p>
<br />

<h2>Step 4: Access Virtual Machines using Remote Desktop Protocol</h2>

<p>
<img src="https://i.imgur.com/Ef2FPCZ.png" height="80%" width="80%" alt="Remote Desktop Protocol"/>
</p>
<p>
The last step is to connect to the virtual machines using Remote Desktop Protocol. I will do this by clicking on one of the virtual machines, and locating the public IP address for it. This is the number I will enter when opening up "Remote Desktop Protocol" from the start menu. After clicking "connect", I'll enter the username and password that I created when creating the virtual machine to log in. Once this is done, a fresh Windows screen should appear next. </p>

<p>
<img src="https://i.imgur.com/6sPt7zQ.png" height="80%" width="80%" alt="log in"/>
</p>
<br />
