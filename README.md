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
Above there you will see the Public IP address and we are going to copy that and connect it to the remote Desktop. 
<p>
<img src="https://i.imgur.com/H0RUjTt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As of this tutorials I'm sure Mac but if you are using windnow the screen might appear slictly different. 
</p>

<p>
  Now we are connected, let us enable IIS (Internet Information Services ) ISS is aMicrosoft web server that runs on Windows operating system and is used to exchange static and dynamic web content with internet users. IIS can be used to host, deploy, and manage web applications using technologies such as ASP.NET and PHP.
  
Start Menu > Windows Feature > Internet Information Services > World Wide Web Services > Application Development Features > CGI

<img src="https://i.imgur.com/rpgUYQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p>
To check whether CGI is working of not, go to the web broswer and search 
  127.0.0.1 and if it appear like the image below then you are all set. </p> 
<img src="https://i.imgur.com/g1j6kIs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p>
First we will download Php manager from <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">download</a>
Then continues to download the Rewrite Module <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view">Rewrite Module </a>
Rewrite Module and Create the directory C:\PHP

  <img src="https://i.imgur.com/MJ2RzHS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p>
    we will going to continues to download 
 <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view" >PHP file</a> we will rIght click on the file and click ( Extract all) 

  <img src="https://i.imgur.com/f5GHARp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p>
  Then our destination is going to be in “PHP” folder the one that we created earlier. Download VC VC_redist.x86.exe
  <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view" >VC_redist.x86.exe</a>


  <img src="https://i.imgur.com/68jirjC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p> Download MySQL 5.5.62 <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view"> MySQL 5.5.62 </a> --> Typical install 
You will have to set up a root password Go to window (IIS) 
Rightclick ( run as administrator) --> Click on PHP manager ( register) 
Look for PHP folder --> Click on php.cgi 

  <img src="https://i.imgur.com/45mdfSR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
  
<p> Download  <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> osTicket v1.15.8 </a> 
  Install osTicket v1.15.8
Double click the download link there you will find “ upload and scripts” folder 
The goal is to drop “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
<img src="https://i.imgur.com/ZAgZEkB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

</p>
  
<p> Go to IIS 
Click on site 
Click on default and then osTicket 
after that On the right, click “Browse *:80”
<img src="https://i.imgur.com/Lo2cgyo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/ZgBvFmr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p> 
- Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
  
Click “Enable or disable an extension.”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

<img src="https://i.imgur.com/6ViYftz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

</p>




</p>


<br />
