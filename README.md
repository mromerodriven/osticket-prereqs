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
- SQL Database

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
<p>
-Download [osTicket zip](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)<br>
-Drag "Upload" folder from zip file to "C:\inetpub\wwwroot" <br>
-Rename that upload folder to osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/FFgeiQU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS. On the left side, navigatge to Sites>Default Web Site>osTicket. Then on the right click on "Browse *.80 (http)".
</p>
<br />

<p>
<img src="https://i.imgur.com/MXMccKK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When installed correctly, your screen should look like this. <br><br>
Go back to IIS click on PHP Manager>Enable or diable an extension <br>
Enable the follow: <br>
-Enable: php_imap.dll<br>
-Enable: php_intl.dll<br>
-Enable: php_opcache.dll<br>
Next, Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/jpms4hA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br>From Properties>Security>Adavanced Disable inheritance -> Remove All then New Permissions -> Everyone -> All<br>
</p>
<p>
<img src="https://i.imgur.com/7gf1rkj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p><br><br>
<b>For the final steps in the installation process, we're going to set the osTicket in the browser</b>
</p>
<p>
<img src="https://i.imgur.com/P0iRbv6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate back to this screen. After refreshing the page, it should look like this. Let's click continue and proceed with osTicket install.
</p>
<br />

<p>
<img src="https://i.imgur.com/dHx27AR.png" height="80%" width="80%"/>
</p>
<p>
Fill in the system settings and the admin user info and we'll come back to this step in just a moment. <br><br>
Next we'll set up HeidiSQL, the database client. <br>
-Download and install [HeidiSQL](https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe) <br>
-Open Heidi SQL>Create a new session, root/Password1>Connect to the session>Create a database called “osTicket”
<p>
<img src="https://i.imgur.com/f5z4B3X.png" height="80%" width="80%"/>
</p>
<p>
<img src="https://i.imgur.com/XL4Cr1l.png" height="80%" width="80%"/>
</p>
</p>
<br />

<p>
<img src="https://i.imgur.com/9AzszmE.png" height="80%" width="80%"/>
</p>
<p>
Go back to the osTicket browser settings and finish inputting the info for the Database settings.
</p>
<br />

<p>
<img src="https://i.imgur.com/cEqp7hI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click install now and...CONGRATULATIONS! You've successfully installed osTicket on the server.
</p>
<br />

<p>
A couple of clean up items: Navigate to C:\inetpub\wwwroot\osTicket and delete the "Setup" folder at this destination.<br>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php<br>
-Properties>Security>Advanced>Select the "Everyone" user>Click Edit>Only Select "Read & execute" and "Read" and click OK>Apply>OK>OK

</p>
<br />
<p>
Check your work by logging in as admin [here](http://localhost/osTicket/scp/login.php)

</p>
<br />

<p>
<img src="https://i.imgur.com/8eswxl6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
