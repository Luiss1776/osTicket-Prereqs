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

By enabling IIS, We will first hit the bottom left windows tab & open the Conrtroll section. We will then go to programs and click, "Turn windows feature on or off." Once Clicking, find the, "Internet Information Services, expand it, Then expand the world wide web tab. Finally, Expand application Developer tab. Finally, Check the CGI button & Press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back end web programming language that allows osTicket to run off a web browser. 
  
We will now download the "PHP manager for IIS" by using the link provided above. Start by clicking, "Download PHP manager," it will automatically open a new web browser. Hit the download button. When done, the file will be in your download tabs in the c-drive of my computer. Download the PHP manager file, and agree with all the terms. We have now downloaded the PHP manager into our operating system.  
</p>
<br />

<p>
<img src="https://i.imgur.com/pmwpPEu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
REWRITE MODULE 

Go back to link provided. Click link to install rewrite module and download it should open in a new browser automatically. Press Download anyways once it’s finished Loading. Once installed go to downloads tab in windows Find rewrite module  in the downloads tab. Accept with terms, & install, press finished 
</p>
<br />

<p>
<img src="https://i.imgur.com/ws1wlka.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
CREATING DIRECTORY C:\PHP 

Go to c windows c drive tab. Right click and open new folder and call it PHP. from installation files download PHP and unzip the contents into c:\PHP. click link provided. Once clicked it should open a new web browser automatically. Press the download icon on the top right, next to blue sign in logo. Once done, go back to downlaods tab in my computer. Right click the PHP 7.3.8file and press extract all. Once done, hit the browse button for destination. Click this PC, C-drive, PHP, Select folder, and then press extract. 
</p>
<br />


<p>
<img src="https://i.imgur.com/Gx8ryBV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VC_REDIST DOWNLOAD
  
From the installation file link above, click download and install VC_Redist. Once done, go back to downloads on my computer and click the VC_Redist file. Agree with any terms and agreements and finish intalling. the following downloads in the download folder should look like the image above. 
  
</p>
<br />

<p>
<img src="https://i.imgur.com/IVpLg40.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Downloading MySQL 
  
From the installation files, download and install my SQL 5.5.62. Go back to downloads & click the MySQL file. Click finish, press next, click standard configuration, click next until you get to password. Your username will be Root, Then Create a password. Press next and then execute.
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
<img src="https://i.imgur.com/ws1wlka.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DOWNLOADING osTicket 

 
</p>
<br />
