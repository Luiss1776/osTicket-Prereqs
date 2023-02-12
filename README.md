<p align="center">
<img src="https://i.imgur.com/CQ7wN8b.png"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2> All Links Provided by: Josh Madakor 🧑‍💻</h2>

- ### [Links for installing Prerequisites for osTicket 😊](https://docs.google.com/document/d/12QH7yrsaiUfYNOgZK7KgTSZQSJ-HYTSVcGFildWMRig/edit#)

<h2>Environments and Technologies Used 💻</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used  </h2>

- Windows 10 🪟</b> (21H2)

<h2>List of Prerequisites 📝</h2>

- Enable Internet Information Services (IIS)
- Install Web platform Installer 
- Install My SQL set up username and passwords
- Install C++ Redistributable
- Configure Permissions & install Os Ticket 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/h4d50AY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enabling IIS 

By enabling IIS, We will first hit the bottom left windows tab & open the Control section. We will then go to programs and click, "Turn windows feature on or off." Once Clicking, find the "Internet Information Services, expand it, Then expand the world wide web tab. Finally, Expand the application Developer tab. Finally, Check the CGI button & Press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser. 
  
We will now download the "PHP manager for IIS" by using the link provided above. Start by clicking, "Download PHP manager," it will automatically open a new web browser. Hit the download button. When done, the file will be in your download tabs on the c-drive of my computer. Download the PHP manager file, and agree with all the terms. We have now downloaded the PHP manager into our operating system.   
</p>
<br />

<p>
<img src="https://i.imgur.com/pmwpPEu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
REWRITE MODULE 

Go back to the link provided. Click the link to install the rewrite module and download it. The link should open in a new browser automatically. If any pop-ups occur, press download anyways. Once installed, go to the downloads tab in file explorer and find the rewrite module inside the downloads tab. Accept the terms, install, and press finished. When done the rewrite module will successfully be installed. 
</p>
<br />

<p>
<img src="https://i.imgur.com/ws1wlka.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
CREATING DIRECTORY C:\PHP 

Go to the c windows c drive tab. Right-click and open a new folder and call it PHP. From the installation files link above, download PHP and unzip the contents into c:\PHP. Once clicked it should open a new web browser automatically. Press the download icon on the top right, next to a blue sign-in logo. Once done, go back to the downloads tab on my computer. Right-click the PHP 7.3.8 file and press extract all. Once done, hit the browse button for the destination. Click this PC, C-drive, PHP, Select the folder, and press extract. 
</p>
<br />


<p>
<img src="https://i.imgur.com/Gx8ryBV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VC_REDIST DOWNLOAD
  
From the installation file link above, click download and install VC_Redist. Once done, go back to downloads on my computer and click the VC_Redist file. Agree with any terms and agreements and finish installing. The following downloads in the download folder should look like the image above. 
  
</p>
<br />

<p>
<img src="https://i.imgur.com/IVpLg40.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Downloading MySQL 
  
From the installation files, download and install my SQL 5.5.62. Go back to downloads & click the MySQL file. Click finish, press next, click standard configuration, and click next until you get to the password. Your username will be Root, then Create a password. Press next and then execute.
(My SQL CREATES A DATABASE FOR YOU TO STORE TICKETS ON for osTicket.

CONFIGURATION OF IIS IS BELOW  
  
Opening IIS As admin. Register PHP from within IIS
INSTALL OSTicket
Open windows Tab bottom left 
Right Click IIS run as admin 
Once opened you will see PHP manager 
Click it, you will see PHP is not enabled 
Click register new PHP version 
Click browse (The 3 dots button) 
Open PHP folder, then click PHP-CGI
Press done or Ok 
</p>
<br />

<p>
<img src="https://i.imgur.com/9Bc5nfC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DOWNLOADING osTicket 

Download OsTicket from the installation files 
Copy and extract the upload folder into the c:\inetpub\wwwroot, rename “upload” to osTicket 
Opening the downloads folder, open two file explorer folders next to each other,
On one of the  file explorer folders, you will want to open, This Pc, followed by Windows C:, Inetpub, and then wwwroot on the other File explorer tab you will want to open, this PC, Downloads, osTicket, and finally drag the “Upload” folder over to the other file Explorer tab to create a new file into the wwwroot. Next rename the upload file from wwwroot to osTicker. Once rename go back to IIS and restart the server  
</p>
<br />

<p>
<img src="https://i.imgur.com/l7MPg1A.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring the IIS permissions. 
  
Go to sites inside IIS default. Default OsTicket On the left hand side, Expand sites, default, and then is ticket, on the right we will click browse *80, once clicked you will be redirected to the OsTicket web browser. Next step notice extensions are not enabled with the red  ❌ , X’s. so we’re going to enable these permissions inside of IIS and make them work. Go back to IIS, go to sites, default web site, OsTicket and click the php manager
  
Double click PHP manager, bottom link click enable or disable an extension highlighted in blue. Now we are going to enable all of these PHP extensions. Scroll down until you see a php_imap. Click on it, and at the top right press enable. We will do the same for php_intl.dll and PHP_opache.dll. Once done go back to osticket web browser and refresh it. It Should still have two red X marks for the bottom two everything else should have green check marks. 

Furthermore, We will now rename the ost-config.php file! We will go to file explorer at the bottom of the windows bar. Go into the wwwroot, click osTicket, scroll down to the include folder. Open it and scroll down to the ost-sampleconfig.php folder. We will rename this folder and just simply erase the sample part

Finally, We will now  adjust the permissions, so anybody can adjust the file the way they want too. We will right click the Ost-config file and go to properties, go to security, go to advance, and then will just disable inheritance so it stops inheriting permissions from its parent, and then will remove all permissions and we’re going to add permissions. Click select a principal,. In the box we will type “everyone” click check names and press OK.  Once done we will the check mark box next to, “full control” and press ok, apply ok and ok. Ost-config now everyone has permissions to it.

</p>
<br />

<p>
<img src="https://i.imgur.com/ovL9d46.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket signup

Fill out any information needed to make an osTicket account. Make sure to write down the osTicket information you may fill out to create any accounts. However, before we continue, we need to setup our database in Heidi sql. 

In the files download link above, we will download Heidi SQL. Once downloaded you will continue to press next until the final install. Once installed we will create a new database for Heidi by clicking the green tab at the bottom left of the Heidi browser. Sign in with your, "mySQL username' and "password" created from mySQL in the previous steps and press open. We will now need to create a new database for osticket. Inside the HeidiSQL on the top left, right click the “unnamed” tab and scroll down to 'create new", and click “database.”  We will name the new database, "osTicket" and press ok. Your new database is now ready to go and to be typed into the osTicket web browser page of osTicket. When done press “install now” and your account will be be made for osTicket. 

Final step For clean Up. 

For clean up we will delete the c:\inetpub\wwwroot\osTicket\setup. By doing this we will go into file explorer tab in my windows. Scroll to This PC, open windows C, open inetpub, open wwwroot, open osticket, and right click the setup folder and click delete. Lastly, we will set the permissions back to “read only” in the ost-config.PHP file. by doing this, we will go into the file explorer, go into this PC, windows C, inetpub, wwwroot, osTicket, the include folder, and right click on the OST-Config.php file. Go to properties, and then security. Scroll down to the advance button and go to the "everyone file" and press edit. Once done, uncheck the boxes, Full control, modify and write. Press ok, apply and then ok.

We have now successfully installed the prerequisite for osTicket. 😊
  
🤓 Admin Login Link: http://localhost/osTicket/scp/login.php
  (To add and change things)
  
📝 End-user link, to create tickets for osTicket: http://localhost/osTicket/
  
</p>
<br />
