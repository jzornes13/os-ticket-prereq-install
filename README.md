# osticket prereq-install
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

- Installation files to download- https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- An active azure subscription( free trial)
- Azure virtual machine running windows operating system

<h2>Installation Steps</h2>

- Log into azure and click resource group
- Name this group RG-osTicket
- We used west US 3
- Click create
- Go back to azure
- In the header or center of the page click create virtual machine.
  
<p>
<img src="https://imgur.com/0QMrH4G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1
    
- Pick the resource group we just created RG-osTicket
- Name your VM anything you want in this case we named it VM-osticket
- Change the region to your own, we used west US 3
- Under image we chose windows 10 pro
- Choose the size of the server taking into account what you will be using it for. we chose Standard v3- 4 16gb memory
- Create a username and password (just remember your credentials!)
- Make sure to check your box (bottom left)
- We can go ahead and skip everything else and click review/create
- If you get the go ahead in the form of "validation passed" click create and were good to go, let it set up your machine.

</p>
<br />

<p>
<img src="https://imgur.com/tbajTdo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2

- Install / Enable IIS in Windows WITH CGI and Common HTTP Features 
- Go to the control panel -> program -> turn on/off
- Expand World Wide Web Services -> Application Development Features ->[X] CGI
- In the Common HTTP Features ->click all
- Test by searching this in google 127.0.0.1, you should see the 2nd image below(internet information services)


<p>
<img src="https://imgur.com/luYtLQI.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
</p>
<p>
Iss cgi
</p>
<br />

<p>
<img src="https://imgur.com/wc9UMFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
127.0.0.1

- Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

</p>
<br />

<p>
<img src="https://imgur.com/oKESqOj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
PHP

- Download and install the Rewrite Module (rewrite_amd64_en-US.msi)

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
Rewrite install

-  In download files, right-click, or top right there is an exclamation point in a triangle, click the 3 dots on the right of that message, press keep, then hit show more, click keep and keep anyway.
-  Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), right- click and press extract all -> unzip the contents into C:\PHP we just made in c drive.

</p>
<br />

<p>
<img src="https://imgur.com/1x45G1N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
PHP 7.3.8 install

- Download and install VC_redist.x86.exe


</p>
<br />

<p>
<img src="https://imgur.com/R9r8ELs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VCredist
  
- Download and install mySQL 5.5.62
- Do a typical setup when asked
- Launch configuration wizard
- Use standard configuration
- Set up user name a password


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
Sql5.5 config
  
- Search IIS in the start menu, right click and run as administrator
- Double click the php manager
- In blue click register PHP version
- Browse to the PHP folder we created on c drive
- Click php-cgi at bottom(if you don't see it in the right bottom corner of that box hit the down arrow and all files)
- Recommend restarting the server whenever you do this, in the ISS-osticket home box, click on the name of the server on the left then on the right there is a restart button in blue under the actions tab.

</p>
<br />

<p>
<img src="https://imgur.com/kZSBCTi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Register php in iss

-  Download and install osticket from the installation files.
-  Open 2 file explorer windows side by side
-  Extract and copy the file named upload to c:\inetpub\wwwroot by going to downloads, double click osticket
-  In the second file explorer window find c:\inetpub\wwwroot
-  Then just drag the file "upload" into c:\inetpub\wwwroot
-  In the root folder(c:\inetpub\wwwroot) rename the file "upload" to "osTicket" by right click rename or slowly clicking 2x on the name
-  Reload the server in the ISS-osticket home box, click on the name of the server on the left then on the right there is a restart button in blue under the actions tab.

</p>
<br />

<p>
<img src="https://imgur.com/Up9lYlE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure osTicket

-  Go to sites in ISS (left side) -> default -> osTicket, then on the right in blue click browse *80(http).
-  You should see the picture below, if you have an error message restart the lab or figure out what you did wrong
</p>
<br />

<p>
<img src="https://imgur.com/qyUhCug.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket installed and working

-  There will be some extensions not enabled indicated by a red X
-  Go back to ISS -> sites -> default -> osticket
-  Double click PHP Manager
-  Enable: php_imap.dll
-  Enable: php_intl.dll
-  Enable: php_opcache.dll
-  Restatrt the server again and the web page saying thank you for choosing osTicket
-  Observe some of the red X are gone now

</p>
<br />

<p>
<img src="https://imgur.com/t2I2Bkr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Os configure name
</p>
<br />

<p>
<img src="https://imgur.com/tmxMRCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Os enable extensions

-  Rename ost-sampleconfig.php file
-  In file explorer search  C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename by taking the "sample" out of the name
-  It should look like this C:\inetpub\wwwroot\osTicket\include\ost-config.php when complete
-  We will assign permissions to this fil(ost-config.php) by finding it in the c drive -> inetpub  -> wwwroot  -> osticket  -> include
-  Right click ost-config.php  -> properties  -> security  -> Advanced  -> disable inheritance(bottom left)  -> remove all permissions
-  Now we will click add  -> select a principal(top left in blue)  -> type everyone  -> check names  -> click full control  -> ok  -> apply  -> ok  -> ok

</p>
<br />

<p>
<img src="https://imgur.com/cnEA4Ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ost configure permissions
</p>
<br />

<p>
<img src="https://imgur.com/ocXvQ02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ost configure everyone permissions

-  Continue Setting up osTicket in the browser (click Continue)
-  Name Helpdesk (Josh help desk) (example)
-  Default email (receives email from customers) josh@helper.com (example)
-  Write down whatever you put in to remember just in case
-  Admin user and email again whatever you want
-  Now we have to set up heidi SQL
-  From the Installation Files, download and install HeidiSQL.
-  Open Heidi SQL
-  Accept everything and launch
-  Create a new session(bottom left button), remember user name is root and our password is Password1
-  Connect to the session by pressing open button
-  In Hedi SQL right click "unnamed" -> create new -> database -> name osTicket -> ok -> minimize that window and go back to osTicket setup page in your browser 


</p>
<br />

<p>
<img src="https://imgur.com/cRJn71i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Heidi sql install

-  Continue Setting up osticket in the browser under database settings
-  MySQL Table Prefix: ost_
-  MySQL Hostname: localhost
-  MySQL Database: osTicket
-  MySQL Username: root
-  MySQL Password: Password1
-  Click “Install Now!” you should see the second picture down if so congratulations!!


</p>
<br />

<p>
<img src="https://imgur.com/9SpxxQD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Heidi database
</p>
<br />

<p>
<img src="https://imgur.com/DX7rJ7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket installed

-  Now we are going to clean up some files
-  Search the c drive for C:\inetpub\wwwroot\osTicket\setup and right-click the "setup" folder and delete 
-  In the same screen find the "include" folder double click, find ost-config.PHP again -> right click -> properties -> security -> advanced -> highlight everyone -> edit -> un-click all the boxes EXCEPT “Read”  and "read & execute" -> ok -> apply -> ok -> ok.

</p>
<br />

<p>
<img src="https://imgur.com/PY989nn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ost cleanup read only

-  Now we will make sure everything is working correctly by copy and pasting this URL (in your normal browser) http://localhost/osTicket/ 
-  Log in using whatever credentials you created for osTicket
-  Hopefully it worked congratulations! 
</p>
<br />

<p>
<img src="https://imgur.com/dBnSFjp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket installed!
</p>
<br />

