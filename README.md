<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Internet Information Services (IIS)
- Microsoft Web Platform Installer
- PHP Manager
- My SQL
- C++ 2008 Redistributable
- osTicket 
- HeidiSQl

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/qZXyAd1.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: In Microsoft Azure click "Virtual Machines" on the homepage.
</p>
<br />

<p>
<img src="https://i.imgur.com/PGuhTO9.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Click "create" then click "Azure Virtual Machine"
</p>
<br />

<p>
<img src="https://i.imgur.com/BZocOS9.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Once you are done setting the VM up. Copy the Public IP Address.
</p>
<br />

<p>
<img src="https://i.imgur.com/Yb0QJpW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: In the start menu search for "Remote Desktop Connection". Once that opens paste the IP Address and login with the username and password you used to create the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/3ZPsC7k.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: When your VM is booted up, search "Control Panel" in the start menu. Then in the Control Panel go to Programs. In Programs under Programs and Features click "Turn Windows features on or off". Lastly, make sure "Internet Information Services" is enabled. 
</p>
<br />

<p>
<img src="https://i.imgur.com/QHRalLT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Install Web Platform Installer. Once that is done installing, open the program and add MySQL 5.5. The username will be root and password will be Password1 for later use.
</p>
<br />

<p>
<img src="https://i.imgur.com/KOY1t2w.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Add all simple versions of x86 PHP until version 7.3. After adding all the versions there may be some failures when installing. You may have to manually install PHP version 7.3.8, PHP Manager, and Microsoft Visual C++ 2008 Redistributable. (Note: you may have to extract some of these files)
</p>
<br />

<p>
<img src="https://i.imgur.com/7E7cq0x.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8: Download osTicket and extract the files. Once extracted copy the "upload" folder into c:\inetpub\wwwroot file and rename it to "osTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/oE2VzvQ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9: Reload IIS. On the left side click OsTicket > Sites > Default web site > osTicket. Then on the right side of the screen under "Manage Folder" open Browse *:80. This will open osTicket in your web browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/6ENh2o5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10: Go back to your ISS and open "osTicket". In the osTicket menu under PHP Extensions click "Enable or disable an extension". 
</p>
<br />

<p>
<img src="https://i.imgur.com/xM25M4y.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 11: In PHP Extensions enable "php_imap.dll", "php_intl.dll", "php_opcache.dll". Note: Some of these may be enabled by default. 
</p>
<br />

<p>
<img src="https://i.imgur.com/yg8fqMl.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 12: Go back into your File Explorer. Open the osTicket folder. Rename the "ost-sampleconfig.php" file to "ost-config.php".
</p>
<br />

<p>
<img src="https://i.imgur.com/YXb5SFz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 13: Right click the ost-config file and click properties. Under the security tab click "Disable inheritance" and remove all.
</p>
<br />

<p>
<img src="https://i.imgur.com/FCus9Ia.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 14: Add a new permission. Under Principal select "Everyone" > Type "Allow" > Permissions enable "Full Control" (this should select all permissions).
</p>
<br />

<p>
<img src="https://i.imgur.com/9grDOsu.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 15: Download and install heidiSQL. Once completed open the program and click "new" on the bottom left of the program. (username will be "root" and password will be "Password1").
</p>
<br />

<p>
<img src="https://i.imgur.com/MFfsrjT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 16: In the session right click "Unnamed" then click "create new" and make a Database.
</p>
<br />

<p>
<img src="https://i.imgur.com/o3fOeGx.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 17: Continue on your Internet Browser to finish setting up osTicket. Remember for MySQL the username is "root" and password is "Password1". After setting everything up click "Install". After installing you can login into the admin panel by clicking the link under "Your Staff Control Panel".
</p>
<br />
