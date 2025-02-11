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

- Setup a Virtual Machine in Azure
- Install the osTicket requirments
- Install osTicket
- Do the after-installation requirments of osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/e55d42d8-272a-4018-bc4b-904c3fe6d70a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/f46713f2-ca4c-4472-a95c-f55aa9f544ee" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/ca103879-66a3-4fa9-97bc-e45a38ee9b4e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First we need to create a resource group for our osTicketing system. Go to "portal.azure.com", create an account and then create a resource group. Next we will make a Virtual Machine for Windows 10. It needs to have at least 4 CPU cores to run efficiently. Give the VM a name and make sure to apply a username and password for the user login into our windows vm. Also click the checkbox that ensures you have an "eligible Windows 10/11 license key". Then we can continue. After that click next and then click create at the bottom left of your screen.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4b38aa5e-9eb5-4564-ad9a-3a026423d43d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we need to login to our Vm with the given IP from the Azure Virtual Machine Portal. Open Remote Desktop from your windows computer or through the Remote Desktop app from MacOS and put in the ip and also type in the username and password we made for the Windows 10 VM and click connect. Next we need to actually install osTicket itself, from there we will install all the dependencies for it. Download the osTicket form this link "https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD". It will download a zip file which you can right click and click extract here and click next until it's extracted and unzipped. Then we can install the program from inside that folder. You can also delete the downloaded zip file as we do not need it. </p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2e9a0dff-e845-4e2e-9393-7f01d4cfb5a7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/2246f4f2-5d6a-4395-98d2-2c6bd8e552c2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will now install or enable IIS in windows. You should have these files from the extracted zip file. From here we'll start the install process. Here are the steps:
Install / Enable IIS in Windows WITH CGI:
- Open control panel and click on Uninstall or change a program, on the left side click on turn windows features on or off. From there we will find World Wide Web Services, and enable it, we will then find Innternet Information Services, then find Application Development Features and then in that folder we will see CGI which we will enable that. Then we can continue the installation process.

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root

</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/eb0beade-a15a-44fa-8d8d-b51085c51e01" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At this point we have successfully installed osTicket and are ready to configure it for our needs.
</p>
<br />
