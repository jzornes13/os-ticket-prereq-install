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
iss cgi
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

-  in download files, right-click, or top right there is an exclamation point in a triangle, click the 3 dots on the right of that message, press keep, then hit show more, click keep and keep anyway.
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
- recommend restarting the server whenever you do this, in the ISS-osticket home box, click on the name of the server on the left then on the right there is a restart button in blue under the actions tab.

</p>
<br />

<p>
<img src="https://imgur.com/kZSBCTi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
register php in iss

-  download and install osticket from the installation files.
-  open 2 file explorer windows side by side
-  extract and copy the file named upload to c:\inetpub\wwwroot by going to downloads, double click osticket
-  in the second file explorer window find c:\inetpub\wwwroot
-  then just drag the file "upload" into c:\inetpub\wwwroot
-  in the root folder(c:\inetpub\wwwroot) rename the file "upload" to "osTicket" by right click rename or slowly clicking 2x on the name
-  reload the server in the ISS-osticket home box, click on the name of the server on the left then on the right there is a restart button in blue under the actions tab.

</p>
<br />

<p>
<img src="https://imgur.com/Up9lYlE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
configure os ticket

-  go to sites in ISS (left side) -> default -> osTicket, then on the right in blue click browse *80(http).
-  you should see the picture below, if you have an error message restart the lab or figure out what you did wrong
</p>
<br />

<p>
<img src="https://imgur.com/qyUhCug.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osticket installed and working

-  there will be some extensions not enabled indicated by a red X
-  go back to ISS -> sites -> default -> osticket
-  double click PHP Manager
-  Enable: php_imap.dll
-  Enable: php_intl.dll
-  Enable: php_opcache.dll
-  restatrt the server again and the web page saying thank you for choosing osTicket
-  observe some of the red X are gone now

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
<img src="https://imgur.com/tmxMRCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
os enable extensions

-  Rename ost-sampleconfig.php file
-  in file explorer search  C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename by taking the "sample" out of the name
-  it should look like this C:\inetpub\wwwroot\osTicket\include\ost-config.php when complete
-  we will assign permissions to this fil(ost-config.php) by finding it in the c drive -> inetpub  -> wwwroot  -> osticket  -> include
-  right click ost-config.php  -> properties  -> security  -> Advanced  -> disable inheritance(bottom left)  -> remove all permissions
-  now we will click add  -> select a principal(top left in blue)  -> type everyone  -> check names  -> click full control  -> ok  -> apply  -> ok  -> ok

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

-  Continue Setting up osTicket in the browser (click Continue)
-  Name Helpdesk (Josh help desk) (example)
-  Default email (receives email from customers) josh@helper.com (example)
-  write down whatever you put in to remember just in case
-  admin user and email again whatever you want
-  now we have to set up heidi SQL
-  From the Installation Files, download and install HeidiSQL.
-  Open Heidi SQL
-  accept everything and launch
-  Create a new session(bottom left button), remember user name is root and our password is Password1
-  Connect to the session by pressing open button
-  in Hedi SQL right click "unnamed" -> create new -> database -> name osTicket -> ok -> minimize that window and go back to osTicket setup page in your browser 


</p>
<br />

<p>
<img src="https://imgur.com/cRJn71i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
heidi sql install

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
heidi database
</p>
<br />

<p>
<img src="https://imgur.com/DX7rJ7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
os ticket installed

-  now we are going to clean up some files
-  search the c drive for C:\inetpub\wwwroot\osTicket\setup and right-click the "setup" folder and delete 
-  in the same screen find the "include" folder double click, find ost-config.PHP again -> right click -> properties -> security -> advanced -> highlight everyone -> edit -> un-click all the boxes EXCEPT “Read”  and "read & execute" -> ok -> apply -> ok -> ok.

</p>
<br />

<p>
<img src="https://imgur.com/PY989nn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
ost cleanup read only

-  now we will make sure everything is working correctly by copy and pasting this URL (in your normal browser) http://localhost/osTicket/ 
-  log in using whatever credentials you created for osTicket
-  Hopefully it worked congratulations! 
</p>
<br />

<p>
<img src="https://imgur.com/dBnSFjp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osticket installed!
</p>
<br />

