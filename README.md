# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create an Azure Virtual Machine
- Log into the VM RDP
- Download and Install osTicket
- Assign permissions
  

<h2>Installation Steps</h2>
To start we need to create a Windows 10 Azure Virtual Machine
<p>
<img width="384" height="464" alt="image" src="https://github.com/user-attachments/assets/a1d7dc3a-da3c-499c-a850-4ae1d174ef3c" />

Don't forget to click in Licensing to confirm your hosting rights

<img width="382" height="433" alt="image" src="https://github.com/user-attachments/assets/d9cc0a7c-0bdf-40d1-b962-5b7b671f237f" />

Let it create a new virtual network, click on review and create and get ready for deployment

<p align left>
<img width="382" height="448" alt="Screenshot 2025-11-26 125007" src="https://github.com/user-attachments/assets/511deb44-fc7c-4071-8e09-823f2fd07c10" />

Validation Passed, click on Create at the bottom of the page 

<p align left>
<img width="392" height="448" alt="Screenshot 2025-11-26 125244" src="https://github.com/user-attachments/assets/aa402835-3a91-43ad-9f06-cfc8aa84c2a4" />

Deployment has been completed

<p align left>
<img width="432" height="275" alt="image" src="https://github.com/user-attachments/assets/b4213dfb-7ba0-4a6c-867f-b11460cab982" />

<h2>Log into the Virtual Machine using Remote Desktop </h2>

Get the public IP address and use your credential to log into the Windows Virtual Machine

<p align left>
<img width="641" height="195" alt="Screenshot 2025-11-26 125550" src="https://github.com/user-attachments/assets/381b9d6c-06c2-4917-86a8-c305b089880a" />

<p align left>
<img width="203" height="122" alt="image" src="https://github.com/user-attachments/assets/3fb62783-b8e0-40a0-80cb-a66ebf1dc701" />
<img width="224" height="164" alt="image" src="https://github.com/user-attachments/assets/e9e1fca9-14a4-4d2a-90d5-ba49e5d1a176" />

You will get this message from Windows, click yes at the bottom of the page to complete the connection

<p align left>
<img width="193" height="196" alt="image" src="https://github.com/user-attachments/assets/34648e53-0329-4f70-95db-b72ce2a297a2" />
<img width="1919" height="1080" alt="image" src="https://github.com/user-attachments/assets/d20f0a9f-cc95-4f66-9ca2-07ee6624d340" />

<h2>Within our Windows Virtual Machine download osTicket</h2>

Open Microsoft Edge and download osTicket osTicket Installation file and unzip them onto the desktop https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download

<p align left>
<img width="1721" height="422" alt="image" src="https://github.com/user-attachments/assets/96fd62a5-523a-428c-a794-8d72f731a32c" />

We are going to use this files to install osTicket and some of the dependencies 
<p aling left>
<img width="1255" height="724" alt="image" src="https://github.com/user-attachments/assets/627c34c6-a81f-4f66-a791-778947c602a5" />

Next install/enable IIS in Windows with CGI, we type the loop back address IP 127.0.0.1 and because the IIS has not been enable yet we get this message 

<p align left>
<img width="1121" height="1016" alt="image" src="https://github.com/user-attachments/assets/92ed1a74-1ff3-4196-921e-5ab6e1e1cd9a" />

To enable IIS, click on Start menu and look for control panel

<p align left> 
<img width="364" height="284" alt="image" src="https://github.com/user-attachments/assets/355e6bb0-7aeb-476b-b9a0-f66568ae1e31" />

Click on Programs, uninstall programs and then on the left side click on Turn Windows features on or off

<p align left>
<img width="518" height="184" alt="Screenshot 2025-11-26 134216" src="https://github.com/user-attachments/assets/265feaad-f89f-4883-ba48-4d41f407fded" />

Click on Internet Information Services, then expand it and look for Worl Wide Web Services and expand it, then click on CGI and click ok and wait to apply changes.
<p align left>
<img width="308" height="274" alt="Screenshot 2025-11-26 141052" src="https://github.com/user-attachments/assets/ac8818d1-bdcd-4da4-9883-488317d6a6e9" />

After the changes requested has been applied you can go back again to loop back address IP 127.0.0.1 and you'll get this page because the IIS and CGI have been enabled in the Windows Virtual Machine and now it will be hosting the osTicket

<p align left>
<img width="1556" height="1012" alt="image" src="https://github.com/user-attachments/assets/d4aabb0c-f029-42df-8983-fc826b725724" />

Now from the installation folder in our desktop, install PHP (PHPManagerForIIS_V1.5.0.msi) and follow the prompts

<p aling left>
<img width="315" height="199" alt="image" src="https://github.com/user-attachments/assets/6317ad9b-2973-4488-aca0-c4fd81573a48" />

From the same folder we are going to install rewrite module (rewrite_amd64_en-US.msi), double click on it and follow the prompts
<p align left>
<img width="315" height="199" alt="ff" src="https://github.com/user-attachments/assets/540cab2f-fea9-49ed-ac60-0bebb4b2de6a" />

Then we are going to create the directory C:\PHP. Open a new file explorer and go to C drive, and create a new folder named PHP

<p aling left>
<img width="317" height="344" alt="Screenshot 2025-11-26 143914" src="https://github.com/user-attachments/assets/e3df8041-40ac-476e-8883-aabb26760f14" />

In the PHP folder created in the C drive, we are going to unzip the file PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and click extract to extract all the files in the PHP folder.
<p align left>
<img width="314" height="236" alt="Screenshot 2025-11-26 144735" src="https://github.com/user-attachments/assets/370b3ce8-84d8-47e2-8e10-bfeb5b7e1acb" />
<img width="1154" height="839" alt="image" src="https://github.com/user-attachments/assets/d65213c9-b97e-43ab-a44c-55cdf62562e2" />



From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe., click install and follow the prompts
<p align left>
<img width="1120" height="653" alt="image" src="https://github.com/user-attachments/assets/3a240c53-2ca9-4c63-8bbe-b11d73e449eb" />


Next, From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) which is a database that will storage all the data required for the osTicket, choose typical and follow the prompts
<p align left>
<img width="1121" height="694" alt="image" src="https://github.com/user-attachments/assets/5c58ab12-ca02-4c5b-9fc8-50f8cee6ede8" />

At some point during the installation, choose standard and then in Modify Security Settings in the new root password type: root and confirm it (this is only for the lab) then click next and execute
<p align left>
<img width="753" height="573" alt="image" src="https://github.com/user-attachments/assets/53d308a7-6e51-425c-a2dd-c3779b881041" />
<img width="750" height="576" alt="image" src="https://github.com/user-attachments/assets/47dac54e-c8d5-4638-a63f-b0c4d398cbbe" />


Now we are going to open IIS as an Admin to 
<p align left>
<img width="353" height="272" alt="image" src="https://github.com/user-attachments/assets/76c38c3c-1a23-4839-8911-32a365bc1605" />
double click on PHP manager
<img width="674" height="475" alt="image" src="https://github.com/user-attachments/assets/f854ecb6-8dab-44c1-a964-41eb3dccb672" />

then click on Register new PHP version and a new window will open, click on the elipsis to browse to drive C:PHP\php-cgi.exe and click OK
<p align left>
<img width="1168" height="802" alt="image" src="https://github.com/user-attachments/assets/a7b28279-0322-4a70-9328-4ba5f6fc37c2" />

Next we are going to install osTicket v1.15.8, from the osTicket Installation folder, a new folder will create named osTicket-v1.15.8 
<p align left>
<img width="1197" height="535" alt="image" src="https://github.com/user-attachments/assets/5f0ef897-aae0-484d-9bb6-0a3b233366e6" />

When files have been unzip we are going to copy the "upload" folder into C:\inetpub\wwwroot and rename it from "upload" to "osTicket"
<p align left>  
<img width="909" height="325" alt="image" src="https://github.com/user-attachments/assets/1ed54e31-d51b-484b-928b-8cdd735e49e6" />

After reload IIS, we click on osticket-vm, then sites, next default web site and finally osTicket and if you have followed the steps you successfully installed osTicket and you will see this webpage
<p align left>
<img width="1577" height="1024" alt="image" src="https://github.com/user-attachments/assets/09dc16d1-c568-40ea-b580-b364d18b83a6" />

If you notice that some of the extension have not been enable, to enable that we have to go back to IIS and double click on PHP Manager, under PHP Extensions click on Enable or disable an extension
<p align left>
<img width="314" height="244" alt="Screenshot 2025-11-26 162742" src="https://github.com/user-attachments/assets/c40f8fab-c1eb-4e32-9fa1-3581f8be431a" />
<img width="278" height="358" alt="Screenshot 2025-11-26 163144" src="https://github.com/user-attachments/assets/bbd32c48-ff08-4e02-bbc5-868643d52f98" />

From the disabled list we look for Enable: php_imap.dll, Enable: php_intl.dll, Enable: php_opcache.dll to enabled them we right click and choose enable 
<p align left>
<img width="220" height="370" alt="Screenshot 2025-11-26 163654" src="https://github.com/user-attachments/assets/cb3eb937-0264-4ee3-aa75-27a514cb61da" />

After enabled the extensions on IIS, refresh the osTicket site in your browser, observe the changes
<p align left>
<img width="1522" height="1002" alt="image" src="https://github.com/user-attachments/assets/f9f8197e-6bf8-49a6-9498-170aab76c90c" />

And finally after configuring osTicket, we are going to rename from ost-sampleconfig.php to ost-config.php
<p align left>
<img width="284" height="271" alt="Screenshot 2025-11-26 164757" src="https://github.com/user-attachments/assets/13ea39ed-5b6e-40ca-8ca5-0a2205a66a6c" />



<h2>Assign Permissions in osTicket</h2>

To be able to make changes in the backend, after finished configuration of the osTicket we have assign permission and to do that we have right click on ost-config.php, click on properties, next click on security, click advanced 
<p align left>
<img width="283" height="275" alt="Screenshot 2025-11-26 165523" src="https://github.com/user-attachments/assets/a53172bf-1fad-4156-a583-0dbd676e16b7" />
<img width="281" height="196" alt="Screenshot 2025-11-26 165852" src="https://github.com/user-attachments/assets/33e209fe-c3c3-49ac-a241-a44d3eedb8b4" />

Click on Add and type "everyone" then click ok
<p align left>
<img width="284" height="166" alt="Screenshot 2025-11-26 170207" src="https://github.com/user-attachments/assets/c0ef1109-5d82-4722-a7f5-10e62fbb2c33" />

Click on Full control then click ok
<p align left>
<img width="278" height="235" alt="Screenshot 2025-11-26 170437" src="https://github.com/user-attachments/assets/99d8cd16-74b9-4fe4-a6d0-323d09e77347" />

And this should be the outcome after allow full control to everyone, apply and then ok
<p align left>
<img width="283" height="197" alt="Screenshot 2025-11-26 170951" src="https://github.com/user-attachments/assets/348aed8d-7619-4d53-8ef3-0e37498738cb" />

Continue Setting up osTicket in the browser (click Continue)
<p align left>
<img width="277" height="244" alt="Screenshot 2025-11-26 171345" src="https://github.com/user-attachments/assets/df4da08b-32cd-4f2a-8e9f-d511e45a2b76" />

Filled out all the information required and use your credentials
<p align left>
<img width="981" height="908" alt="image" src="https://github.com/user-attachments/assets/d3a552be-20d3-4c89-aee8-b5d1b19a7179" />

To install the database for osTicket we have to go back to the osTicket-Installation-Files and double click on HeidiSQL, when it opens skip 
<p align left>
<img width="1162" height="707" alt="image" src="https://github.com/user-attachments/assets/70316942-61ee-4d25-ab6a-b2357ed44023" />
<img width="573" height="678" alt="image" src="https://github.com/user-attachments/assets/cf14ba1d-3883-4af2-857b-57d471b88afc" />

Then click on new on the bottom left, enter your credentials previously created (user: root and password: root) and it will open another window to access the database
<p align left>
<img width="283" height="200" alt="image" src="https://github.com/user-attachments/assets/0c398f3a-8efd-48f4-8b3b-39bae45e21d0" />
<img width="1401" height="407" alt="image" src="https://github.com/user-attachments/assets/bd0bfad9-4b9a-4b8f-9bf7-1dfe0fc8d24f" />

To create the database we have to right click on where it says Unnamed, click on new and create database named: osTicket, then click ok
<p align left>
<img width="377" height="193" alt="Screenshot 2025-11-26 173710" src="https://github.com/user-attachments/assets/c2a38929-a029-4327-8d69-4495c7eaead6" />
<img width="437" height="426" alt="image" src="https://github.com/user-attachments/assets/f3ed77d5-ce12-4d44-b61b-d345aefbf833" />

Go back to our browser to continue with configuration, filled out the database settings with the new database we just created in Heide SQL
<p align left>
<img width="376" height="197" alt="Screenshot 2025-11-26 174331" src="https://github.com/user-attachments/assets/4cb3baca-ce7c-41e9-baaf-c67587e282be" />

Congratulations you have successfully installed your osTicket in your Windows Virtual Machine!
<p align left>
<img width="1602" height="973" alt="image" src="https://github.com/user-attachments/assets/378414fc-0b07-45d9-a8dc-404a7def448b" />



