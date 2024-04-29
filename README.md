<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
Hi there, I am Thaw, an IT Professional. Welcome to my first tutorial on setting up osTicket. This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>What is osTicket? </h2>
-<b>osTicket is an open-source ticketing system designed for managing customer support inquiries. It provides a platform for businesses to efficiently track, prioritize, and resolve customer issues through a centralized interface. With features like customizable ticket forms, automation, and reporting, osTicket helps streamline support operations and improve customer satisfaction.<b>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/4Eri0B7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, we will create a Resource Group (RG) in Microsoft Azure Cloud Service. Think of the resoruce group as a folder. We will name this resource group as "osTickets". I personally used US East to create my RG. Take note of what region you create your RG and will be creating future instances with.
</p>
<br />

<p>
<img src="https://i.imgur.com/SSlHEsa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, it is time for us to create a virtual machine under the RG. Think of the virtual machine as a computer on the internet or harddrive you can access within your own computer. Pretty cool. As before, I will set my VM region to US East. We will be using Windows 10 with 4vCPUs. We can name this VM "VM-osTicket".

Create a username and password for your VM. You will be logining in to it like a regular computer ! So, take notes to not forget your login credentials. I set my username to be "labuser" and set my password to be "Password1". In the real world, never do this. However, for this demonstration it is fine. Great.

Now that our machine is ready, we will connect to it using Remote Desktop Connection. before that, let us grab the public IP address of the VM.
</p>
<br />
<p>
<img src="https://i.imgur.com/dAYYewj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Above there you will see the Public IP address and we are going to copy that and connect it to the remote Descktop. 
<p>
<img src="https://i.imgur.com/H0RUjTt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As of this tutorials I'm sure Mac but if you are using windnow the screen might appear slictly different. 
</p>
<br />
