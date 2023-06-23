# os ticket prereq-install
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

- installation files to download- https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- an active azure subscription( free trial)
- azure virtual machine running windows operating system

<h2>Installation Steps</h2>

- log into azure and click resource group
- name this group RG-osTicket
- we used west US 3
- click create
- go back to azure
- In the header or center of the page click create virtual machine.
  
<p>
<img src="https://imgur.com/0QMrH4G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1
    
- Pick the resource group we just created RG-osTicket
- name your VM anything you want in this case we named it VM-osticket
- change the region to your own, we used west US 3
- under image we chose windows 10 pro
- choose the size of the server taking into account what you will be using it for. we chose Standard v3- 4 16gb memory
- create a username and password (just remember your credentials!)
- make sure to check your box (bottom left)
- we can go ahead and skip everything else and click review/create
- if you get the go ahead in the form of "validation passed" click create and were good to go, let it set up your machine.

</p>
<br />

<p>
<img src="https://imgur.com/tbajTdo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2

- Install / Enable IIS in Windows WITH CGI and Common HTTP Features 
- go to the control panel -> program -> turn on/off
- expand World Wide Web Services -> Application Development Features ->[X] CGI
- in the Common HTTP Features ->click all
- test by searching this in google 127.0.0.1, you should see the 2nd image below(internet information services)


<p>
<img src="https://imgur.com/luYtLQI.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
</p>
<p>
- iss cgi
</p>
<br />

<p>
<img src="https://imgur.com/wc9UMFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
127.0.0.1

- download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

</p>
<br />

<p>
<img src="https://imgur.com/oKESqOj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
PHP

- download and install the Rewrite Module (rewrite_amd64_en-US.msi)

</p>
<br />

<p>
<img src="https://imgur.com/wpD2pqC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
REWRITE

- Create the directory C:\PHP
- go into c drive, right click, new folder, name it PHP

</p>
<br />

<p>
<img src="https://imgur.com/t8hlzF8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
rewrite install

-in download files, right-click, or top right there is an exclamation point in a triangle, click the 3 dots on the right of that message, press keep, then hit show more, click keep and keep anyway.
-  download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), right- click and press extract all -> unzip the contents into C:\PHP we just made in c drive.

</p>
<br />

<p>
<img src="https://imgur.com/1x45G1N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
PHP 7.3.8 install

- download and install VC_redist.x86.exe


</p>
<br />

<p>
<img src="https://imgur.com/R9r8ELs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VCredist
  
- download and install mySQL 5.5.62
- do a typical setup when asked
- launch configuration wizard
- use standard configuration
- set up user name a password


</p>
<br />

<p>
<img src="https://imgur.com/9RNl28P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
SQL 5</p>
<br />

<p>
<img src="https://imgur.com/O8qA6Nl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
sql5.5 config
  
- search IIS in the start menu, right click and run as administrator
- double click the php manager
- in blue click register PHP version
- browse to the PHP folder we created on c drive
- click php-cgi at bottom(if you don't see it in the right bottom corner of that box hit the down arrow and all files)

</p>
<br />

<p>
<img src="https://imgur.com/kZSBCTi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
register php in iss
</p>
<br />

<p>
<img src="https://imgur.com/Up9lYlE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
configure os ticket
</p>
<br />

<p>
<img src="https://imgur.com/qyUhCug.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osticket installed and working
</p>
<br />

<p>
<img src="https://imgur.com/tmxMRCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
os enable extensions
</p>
<br />

<p>
<img src="https://imgur.com/t2I2Bkr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
os configure name
</p>
<br />

<p>
<img src="https://imgur.com/cnEA4Ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
ost configure permissions
</p>
<br />

<p>
<img src="https://imgur.com/ocXvQ02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
ost configure everyone permissions
</p>
<br />

<p>
<img src="https://imgur.com/cRJn71i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
heidi sql install
</p>
<br />

<p>
<img src="https://imgur.com/9SpxxQD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
heidi database
</p>
<br />

<p>
<img src="https://imgur.com/DX7rJ7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
os ticket installed
</p>
<br />

<p>
<img src="https://imgur.com/PY989nn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
ost cleanup read only
</p>
<br />

<p>
<img src="https://imgur.com/dBnSFjp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osticket installed!
</p>
<br />

