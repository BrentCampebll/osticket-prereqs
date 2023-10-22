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

- PHP Manager
- MySql 
- OSTicket
- HeidiSql
- Azure
- Remote Desktop
- PHP Zip file
- Rewrite Module

<h2>Installation Steps</h2>

<p>
<img <a href="https://imgur.com/wahYFhz"><img src="https://i.imgur.com/wahYFhz.png" title="source: imgur.com" />
</p>
<p>
To get started you need to create a Resource Group and Windows 10 virtual machine in Azure.  While creating your virtual Machine create a username and password to login to your virtual machine via remote desktop program.   I need to install/enable IIS with CGI and common HTTP services, As well as IIS management console.  After that I will begin installing the programs listed above in the prequiste section to install OSticket onto our virtual machine. 
</p>
<br />

<p>
<img <a href="https://imgur.com/HSLmzJK"><img src="https://i.imgur.com/HSLmzJK.png" title="source: imgur.com" /></a>
<img <a href="https://imgur.com/LFPBJSZ"><img src="https://i.imgur.com/LFPBJSZ.png" title="source: imgur.com" /></a>
</p>
<p>
Start with  PHPmanager & Rewrite Module are installed.  Create a directory on the C drive of your virtual machine labeled PHP.  Here you will place the files of your PHP zip file that was downloaded earlier. Next we will move on to VC_Redist86 & My SQL.  MySql installition will be typical then standard with a basic password you can remember.  Once these are installed we will open IIS as an administrator by right clicking on the program after a quick search. After registering the CGI PHP file from your PHP folder.  Once done start your IIS server.reload and retYou wll extract OSticket Upload file and placeit in the c:\inetpub\wwwroot, then Rename “upload” to “osTicket”.  Once done reload and restart your IIS server</p>
<br />

<p>
<img <a href="https://imgur.com/JDBgfUN"><img src="https://i.imgur.com/JDBgfUN.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/iopqXXp"><img src="https://i.imgur.com/iopqXXp.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/BRVT5nZ"><img src="https://i.imgur.com/BRVT5nZ.png" title="source: imgur.com" /></a>
</p>
<p>
For thr Final steps of prep i go to default websites the osticket and right click on browse.80 on the right hand side of the screen.  This will open an OSticket Web broswer.  From there i will need to activate prequistes for for OSticket.  Head to the Osticket PHP manager in IIS.  enable these 3 files php_imap, php_intl, & php_opcahe.  Once they have been enabled.  Head to the OSticket folder on the C drive and in the include folder rename ost-sampleconfig to ost-config.  Then disable the inheritance and add a new permission for all to access.  Once these are done continue setup of OSticket in your browser.  After naming your help desk and creating a default email to recieve customer requests. install HeidiSQL.  Here you will create the OSticket database.  Finish the OSticket setup with the database you created in HeidiSQL along with the password and root login.  Dont forget to create the primary user and login.  Once this is done click install now and OStcket is complete</p>
<br />
