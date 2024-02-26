<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)


<h2>List of Prerequisites</h2>

- Setup a Virtual Machine in Azure
- Install the osTicket requirements
- Install osTicket itself
- Do the after-installation configuration of osTicket
- Explore osTicket as a Help Desk Professional
  - Create, interact, and close tickets
- Clean up Virtual Environment in Azure to minimize subscription cost


<h2>Installation Steps</h2>
<p>
<img src="https://i.imgur.com/JgVnHer.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
welcome, we will have to create a Virtual machine using the Microsoft Azure portal. We will be using a VM which is a remote computer. We are using a VM in order to protect our physical machine just in case something breaks. Create a resource group and title it "osTicket".
</p>
<br />




<p>
<img src="https://i.imgur.com/rb02ZOY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, connect to your newly created VM using RDP using the public IPv4 address. If you are a Mac user you will have to download Microsoft RDP.
</p>
<br />




<p>
<img src="https://i.imgur.com/qtEnuWu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will have to enable IIS. Access the control panel then select uninstall a program. Off to the left select "Turn windows features on or off". A list will appear then you will enable Internet Information Services.
</p>
<br />




<p>
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that you have enabled IIS, we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. That link will provide you with all of the materials you need to download osTicket software. Click the link and install the Web Platform Installer.
</p>
<br />




<p>
<img src="https://i.imgur.com/JJ8bZeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you have installed Web Installer Platform, run the program. From inside the application, you are going to install MySQL 5.5. Afterwards, install x86 version of PHP up until 7.3. There are some failed files such as C++ redistributable package as well as PHP 7.3.8 and PHP Manager for IIS those files can be found with the install link.
</p>
<br />




<p>
<img src="https://i.imgur.com/TUGiSKi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next download the osTicket file. Then, extract and copy the "upload" folder into c:\inetpub\wwwroot. And rename the folder to osTicket.
</p>
<br />




<p>
<img src="https://i.imgur.com/fti4XnK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager, go to Sites->Default->osTicket on the right side of the screen click on "Browse*.80". Your default browser should open osTicket webserver.
</p>
<br />




<p>
<img src="https://i.imgur.com/OL91MIc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into IIS manager and enable some extensions. To do this, you have to go to Sites->Default->osTicket Then, double click on PHP manager. Click on "Disable or enable an extension". Enable "php_intl.dll" & "php_opcache.dll", Refresh the osTicket webserver and obsereve the changes "Intl Extension" and it should now be enabled.
</p>
<br />




<p>
<img src="https://i.imgur.com/1nYaYGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php. Rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php. Assign permissions to ost-config.php, and disable inheritance->Removeall. New Permissions->Everyone->all.
</p>
<br />




<p>
<img src="https://i.imgur.com/b0wFxRN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At this point, you are ready to set up your session manager and ready to log in with your SQL credentials.  
</p>
<br />



<p>
<img src="https://i.imgur.com/RmVk3q5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you did everything correct, you should see a webpage opened up "osTicket Installer". Make sure you set up system settings, Admin users and Database settings.
</p>
<br />



<p>
<img src="https://i.imgur.com/ECyNT0h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Congratulations! You have succesfully installed a working osTicket system software and ready to practice handling deffirent service/request tickets. Assign the SLA and the representative or the correct department that handles those tickets, or Escalate them.
</p>
<br />
