<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h2>osTicket - Prerequisites and Installation</h2>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h3>Environments and Technologies Used</h3>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h3>Operating Systems Used </h3>

- Windows 10</b> (21H2)

<h3>List of Prerequisites</h3>

- Have an Active Microsft Azure Account
- Within that Azure Account, Create an Azure Virtual Machine (Windows 10)
- Once operating on the Virtual Machine, Enable and Configure IIS in Windows with CGI and Common HTTP Features. This is necessary to install OSticket! 
- Within that Virtual Machine Install,  Download and install all required files; PHP Manager, Rewrite Module, MySQL, OSticket, HeidiSQL, VC Redist. And OSticket.
  
-  <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Source for All listed Files</a>
- If confused by any of the prerequisites I will be going into it with further detail on the "Installation Steps" portion of this Tutorial.

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  1. (Azure Portal) Using your Active Microsoft Azure account, You're going to create a Windows 10 Pro Virtual Macine. In order for everything to run smoothly you're going to need to create this virtual machine with a minimum of 2vcpus and 16gbs of memory. Once everything is all finished being created you're going to want to connect to your virtual machine. For Windows users you would use the "Remote Desktop App" which can be found by using your computers searchbar. For Mac users, You're going to need to download Microsoft's "Remote Desktop" app from the app store.
 
 2.(Remote Desktop) Once you have opened the Remote Desktop app, you'll be prompted to enter the Public IP address of the Computer you're trying to gain remote access too. This can be found on the Azure Portal when you access your Virtual Machine. Now that you've retrieved your Virtual Machines Public IP address enter that into the remote desktop app along with what credentials you've made for your username and password. You should now have access into your virtual machine and it should be starting up.

 3.(The Files) Make sure you have ALL the files mentioned in the prerequisites ready to be installed. (PHP Manager, Rewrite Module, MySQL, OSticket, HeidiSQL, VC Redist. And OSticket.) I Have sourced them on the "List of Prerequisites" section of this tutorial but before anything we must properly install and configure IIS in your virtual machine.    

  3.(Internet Information Services) IIS is short for Internet Information Services. We must properly install and configure IIS in your virtual machine because this is necessary to install "OSticket". To do this you will need to open up "Programs" from the Control Panel on your Virtual Machine. From there select "Turn Windows features on or off" Another window should pop up, go through that list and look for IIS. You're going to want to make sure the IIS box is "Checked". Then within that list click on "World Wide Web Services. "Application Development Features" will pop up under "World Wide Web Services". Check the box "CGI" off. Next you should also see in the list a "Common HTTP Features", Click on this. Make sure all the boxes under are checked off. 

 4. (Installation Files) Download and Install all the files except for OSticket at this point. There are certain steps and configurations that you need to follow to make sure everything is in the correct place it needs to be and that everything is configured correctly to ensure everything is running the way it's supposed to. I would first start by downloading and installing PHP manager, Rewrite Module (It is a requirement for OSticket to work), and VC Redist. as these are simple installations. Next I would Create a directory for PHP on the local hard drive (C:) By creating a new folder named PHP. Now You're going to want to download PHP. Once it's finished downloading you're going to right-click PHP from the downloads folder, click "extract all" from your list of right-click options, click browse and make the extract destination into your "C:\PHP" folder. Next download and install MySQL. During the installation procress you're going to want to check off that you want to do the Typical Install. At the end of the install you'll be prompted on launching the MySQL Setup Wizard. Make sure that you click on that option. From there you're going to click standard configuration and Install as a Windows Service. Create a password, execute and you're all finished with your Installation files.

 5. (Configuration Inside of IIS) Now that all the prerequisite files have been downloaded its time to configure some things in IIS. To do this open IIS as an Admin by right-clicking the IIS icon and selecting run as admin from the list of options presented. From there you will get access to the IIS Manager. Inside of the IIS manager you will see several programs, click on the "PHP Manager". From the PHP Manager screen you will register a new PHP version. To do this you will browse and open the PHP folder from the C drive. All Finished! KEY NOTE: Whenever you do anything on the IIS Server it is recommended that you restart the server for best results. To do this go to the IIS Manager Homepage and in the Actions Taskbar you're going to click "Restart".
 
 6. (Install OSticket) Being Installing OSticket now that you've finished all the other steps. Once it appears in your downloads folder, open up the C\netpub\wwwroot folder from your C drive. Extract the "Upload" folder from your Downloads folder to the wwwroot folder. Once you're finished with these steps rename the upload folder to "OSticket". Lastly Restart the IIS Server.
    



</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Filler Text
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Filler Text
</p>
<br />
