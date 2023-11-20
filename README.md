<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<!--
<h2>Video Demonstration</h2>
--
- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)
-->
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2) VM

<h2>List of Prerequisites</h2>

- Azure Subscription/Resource Group/VM
- RDP
- PHP Manager for IIS
- osTicket
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/CVqOBcA.png" height="80%" width="80%" alt="Set up your Virtual Network"/>
</p>
<p>
Create your VM. In this example, I created a VM within a Resource Group. In a real-world setting, you may have multiple RGs and VMs.
</p>
<br />

<p>
<img src="https://i.imgur.com/vt6ne8G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, find your Public IP address to prepare to remote connect to your VM. You'll need this IP address and the user name and password you created for this VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZASycCR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log into your virtual maching.</p>
<br />

<p>
<img src="https://i.imgur.com/PZ4kwp5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We need to activate specific Windows features. Open Control Panel > Click on Programs > Click on "Turn Windows features on or off". Your screen should look like this.

Make sure the follow are selected:
-Internet Information Services<br>
-Internet Information Services>World Wide Web Service>Application Development Features>CGI<br>
-Internet Information Services>World Wide Web Service>Common HTTP Features>(Make sure all are selected)<br>
<br>
Then click "OK"
</p>
<br />

<p>
<img src="https://i.imgur.com/Sbcu9FM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Your changes will start installing and applying your IIS web server.
</p>
<br />

<p>
<img src="https://i.imgur.com/aVDlHvT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You know you applied the correct changes when your IIS site looks like this.<br>
Open a browser in your VM and go to "127.0.0.1" to verify this is accurate.
<br><br>
  
-Download and install [PHP Manager](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view) <br>
-Download and install [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view) <br><br>
<img src="https://i.imgur.com/fUvTVN8.png" height="80%" width="80%"/> <br>
-Create the directory C:\PHP  <br>
-Download [PHP Software Zip File](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view) <br>
-Extract PHP zip file to C:\PHP <br>
-Download and install [VC_Redist](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view) <br>
-Download and install [MySQL](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view)  NOTE: Use Standard Configuration for install<br>
-Create and save the "root" user password <br>   
</p>
<br />

<p>
<img src="https://i.imgur.com/OXD9o3f.png" height="80%" width="80%" alt="IIS As Administrator"/>
</p>
<p>
From your start menu, search for "IIS". Right click it and select "Run as administrator"
</p>
<br />

<p>
<img src="https://i.imgur.com/iEiJi1t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Open PHP Manager <br>
-Click "Register new PHP version" <br>
-Browse for "C:\PHP\php-cgi.exe" and click open then click ok
</p>
<br />

<p>
<img src="https://i.imgur.com/YFHpiS1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><br>
-Download [osTicket zip](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) <br>
-Drag "Upload" folder from zip file to "C:\inetpub\wwwroot"
</p>
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
