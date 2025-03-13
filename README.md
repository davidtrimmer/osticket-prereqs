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

- Setup Windows 10 VM in Azure, log in using RDP 
- Setup IIS within Windows VM
- Download osTicket software
- Setup database using HeidiSQL/MySQL  
- Login to osTicket Software

<h2>Installation Steps</h2>

<p>
<img width="784" alt="Screenshot 2025-03-11 at 4 11 45 PM" src="https://github.com/user-attachments/assets/bc24b52e-9a8d-4396-a10a-31286da74465" />
<br />
<p>
 <img width="820" alt="Screenshot 2025-03-11 at 4 12 02 PM" src="https://github.com/user-attachments/assets/a6e70188-121a-4a12-88da-544323892fd9" />
</p>
</p>
<p>
 First, we must create our Virtual Machine in Microsoft Azure. Go to Azure's website, and log in. After you log in, go to Virtual Machines->Create a Virtual Machine. Make sure that your VM has all of the RED starred pieces of info filled in. Under size, you want to make sure that your VM has AT LEAST 2 vCPU's. This will help with the overall speed of the VM. 
</p>
<br/>
<p><img width="454" alt="Screenshot 2025-03-11 at 4 40 14 PM" src="https://github.com/user-attachments/assets/6de15b6c-1e2c-48b9-addb-d59576466185" />
<img width="435" alt="Screenshot 2025-03-11 at 4 40 53 PM" src="https://github.com/user-attachments/assets/32916ca9-e7de-4bfc-9cbb-0f9bada1dfe1" />
</p>
<p>
Next, you need to remote in to the VM using Remote Desktop Protocol. I am running a Mac, so I am using the Windows App. To log in, you need to have the IP address for the Windows VM, copy it into the RDP software, give it a name, and log in using the credentials you would have used when you created the VM. 
</p>
<br/>
<p><img width="1440" alt="VM-OSticket" src="https://github.com/user-attachments/assets/6ba89019-0c7b-4e4d-aa8b-7211588dd232" />
 
</p>
<p>
After getting logged in, I downloaded the osTicket software from the zip file. After I extracted the zip file to the desktop, I paused installing and went ahead and configured the necessary settings to set up IIS. First, hit the start button, type "Control Panel", then go to Programs, click on "uninstall a program". From there, click on "Turn Windows Features on or off." Then, you should see "Internet Information Services" click on both "Web Management Tools" and "World Wide Web Services" as seen in the photo. Hit the plus side under World Wide Web so that way the "Application Development Features" folder opens. Make sure that "CGI" is checked and save the changes.  
</p>
<p>
 <img width="1128" alt="Screenshot 2025-03-11 at 5 09 01 PM" src="https://github.com/user-attachments/assets/554db6d5-827f-48e7-bbb6-7a686eef71e4" />
<br />
 <img width="303" alt="Screenshot 2025-03-11 at 5 11 12 PM" src="https://github.com/user-attachments/assets/8e01300d-0ad4-4c49-a9dc-57c42336faa2" />
 <img width="296" alt="Screenshot 2025-03-11 at 5 26 15 PM" src="https://github.com/user-attachments/assets/612e4205-9a05-45b4-aec5-74f637705495" />
</p>
<br />

<p><img width="1440" alt="Screenshot 2025-03-11 at 5 29 04 PM" src="https://github.com/user-attachments/assets/4e0532d8-47be-4d0e-aa27-7f53a55ec0f1" />
<img width="833" alt="Screenshot 2025-03-11 at 5 31 13 PM" src="https://github.com/user-attachments/assets/60e00be3-e82a-44d1-b547-56bff95e0e56" />
<img width="489" alt="Screenshot 2025-03-11 at 5 32 27 PM" src="https://github.com/user-attachments/assets/f11d98b0-f6a8-4f1b-896c-b6b85caf7ee5" />


</p>
<p>
 Install the PHP Manager for IIS. Install the "rewrite AMD" file as well. 
</p>
<br/>
<p>
 <img width="627" alt="Screenshot 2025-03-11 at 5 34 34 PM" src="https://github.com/user-attachments/assets/190863ac-94f1-4883-96e6-9fecb4fae96f" />
</p>
<p>
 We will now create a "PHP" folder on our VM's C: drive.
</p>
<br/>
<p>
 <img width="1440" alt="Screenshot 2025-03-11 at 5 39 15 PM" src="https://github.com/user-attachments/assets/daf8806a-4ea1-4afc-8703-9d2b6fe4fd22" />
 <img width="588" alt="Screenshot 2025-03-11 at 5 40 03 PM" src="https://github.com/user-attachments/assets/bb12afb0-2202-4867-b3d6-84e4f873372a" />
 </p>
 </p>
 <br/>
<p>
  In the osTicket files that we have been downloading from, we can extract the "PHP folder" to the PHP directory that we made on the C: drive. 
</p>
<br/>
<p>
 
  After unzipping the PHP folder into the PHP directory. We need to download the C++ redistrib from the osTicket downloads. We will also install mySQL5.5.62 (Typical setup, standard configuration, launch config wizard post-install). Use "root" as your username and password.
</p>
<p>
 <img width="1440" alt="Screenshot 2025-03-11 at 6 17 36 PM" src="https://github.com/user-attachments/assets/49bd23c4-14fa-4b44-a78c-45d9008b737e" />
 <img width="1440" alt="Screenshot 2025-03-11 at 6 17 53 PM" src="https://github.com/user-attachments/assets/d81496ee-5652-4f2d-900a-dd57f382bcca" />


</p>

</p>
<p><img width="1440" alt="Screenshot 2025-03-01 at 1 28 27 PM" src="https://github.com/user-attachments/assets/5a86ac97-806f-458c-8778-4f5cd257a67d" /> 
</p>
<p>
Next, open IIS as an admin and you should see this screen.   
</p>
<br />
<p>
<img width="854" alt="Screenshot 2025-03-11 at 6 35 21 PM" src="https://github.com/user-attachments/assets/451243ae-c602-4951-88ae-d7cb4dce5440" />
<img width="1250" alt="Screenshot 2025-03-11 at 6 58 48 PM" src="https://github.com/user-attachments/assets/f08bff9a-e828-477f-a47c-bd60d0b710d8" />
</p>
<p>
Next, we will install osTicket. From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br/>
<p>
 <img width="1440" alt="Screenshot 2025-03-12 at 6 58 32 PM" src="https://github.com/user-attachments/assets/9b3eb21b-dfb6-4712-a5f8-a9310f3e9039" />
</p>
<p>
 After renaming the folder to osTicket. You can reload IIS. Once it has reloaded, you can click on the "sites" folder, then "Default Web store" then "osTicket" folder. After that, on the right hand side, you should see under "Manage folder" you can click on "Browse *.80(http)". Once you click this, you should see the photo above, which will let you know that you installed osTicket correctly. 
</p>
<br/>
<p>
 <img width="648" alt="Screenshot 2025-03-12 at 7 04 21 PM" src="https://github.com/user-attachments/assets/5354e5b8-b7e1-46f4-afdc-c80ab3baad99" />
 <img width="635" alt="Screenshot 2025-03-12 at 7 05 06 PM" src="https://github.com/user-attachments/assets/c915eb05-fb00-4eaf-8baf-f6ef4fcaf620" />
</p>
<p>
 Next, we need to make additional configurations in IIS so that osTicket can run smoothly. First, go back into IIS and access the PHP manager within the osTicket folder in go to "PHP Extensions". Click on "enable or disable and extension". We will need to enable php_imap.dll , php_intl.dll , and php_opcache.dll . Then reload the IIS and view the changes in osTicket. 
 <br/>
 <p>
  <img width="542" alt="Screenshot 2025-03-12 at 7 25 19 PM" src="https://github.com/user-attachments/assets/4ccdd7a1-114b-4d5a-adec-751396dbcf5d" />
  <img width="375" alt="Screenshot 2025-03-12 at 7 26 05 PM" src="https://github.com/user-attachments/assets/79aefa63-01c1-489f-871c-4b4a2df4d9bb" />
  <img width="521" alt="Screenshot 2025-03-12 at 7 24 58 PM" src="https://github.com/user-attachments/assets/9949d1d5-bf76-42fb-943f-6276421c2b84" />
  <img width="315" alt="Screenshot 2025-03-12 at 7 25 07 PM" src="https://github.com/user-attachments/assets/0c2b30d5-dfea-4130-9aee-fe87444e62e9" />
 </p>
 <p>
  Next, we need to rename the "ost-sampleconfig.php" file to "ost-config.php". To do this, go to the osTicket folder that we installed on the "wwwroot" folder that is on the C: drive. Open the osTicket folder, click on the "include" folder, find the "ost-config.php" file and rename it. 
 </p>
 <br/>
 <p>
  <img width="374" alt="Screenshot 2025-03-12 at 7 26 23 PM" src="https://github.com/user-attachments/assets/c4daf71d-5430-41d0-ab31-31d968aabaa5" />
  <img width="785" alt="Screenshot 2025-03-12 at 7 26 40 PM" src="https://github.com/user-attachments/assets/4063e7c2-de98-452c-a67d-685524a23e0e" />
  <img width="728" alt="Screenshot 2025-03-12 at 7 28 06 PM" src="https://github.com/user-attachments/assets/db6d9ec5-6586-40d1-8852-d0671bc78908" />
  <img width="1440" alt="Screenshot 2025-03-12 at 7 28 26 PM" src="https://github.com/user-attachments/assets/292038f5-0c59-436c-a41a-462b751aa5c7" />
 </p>
 <p>
  Now, we need to assign permissions to the ost-config file. To do this, right-click on the file and go to "Properties". Then, click on "Security", then "Advanced", we can "disable inheritance" this will remove any defaulted permissions. Once that is done, click "select a principal" and type in "everyone" this will proper access to osTicket. Go ahead and apply these changes. 
 </p>
</p>
<p><img width="624" alt="Screenshot 2025-03-03 at 10 49 31 AM" src="https://github.com/user-attachments/assets/ffde316e-a3d4-401e-ba66-ecb19ac8de8f" />
</p>
</p>
Now, we can reload our osTicket on our browse and complete the basic set up for the help desk user. 
</p>
<p>
 <img width="697" alt="Screenshot 2025-03-12 at 7 49 41 PM" src="https://github.com/user-attachments/assets/3483fde8-7525-4881-a37d-a51554b4d78b" />
 <img width="608" alt="Screenshot 2025-03-03 at 10 52 57 AM" src="https://github.com/user-attachments/assets/264d6738-54d0-490e-b73c-e53e215e0271" />
</p>
<p>
Next, we will go back to the osTicket downloads that we saved to our desktop, and download and run HeidiSQL. This will house our database on the back end. We will use the username and password of 'root' that we set up previously.
</p>
<br>
<p>
 <img width="592" alt="Screenshot 2025-03-12 at 7 52 07 PM" src="https://github.com/user-attachments/assets/e6edf9f8-ca3a-4b21-bb73-ce971a5a2ba5" />
</p>
<p>
 In HeidiSQL, we will create a database named osTicket. To do this, click on the icon to the left of the text that says "Unnamed" and hit "Create new". Name this osTicket. This should connect our database. 
</p>
<p>
 <img width="1121" alt="Screenshot 2025-03-12 at 7 57 54 PM" src="https://github.com/user-attachments/assets/0f0a58b4-d35b-42af-bfbf-15ca2078c478" />
</p>
<p>
 Next, we can input our information in the "mySQL" portion of the basic configuration in the osTicket browser. in the "mySQL database" box you can fill it in as osTicket, the use 'root' for the username and password. Then click "Install Now".
</p>
<br/>
<p>
 <img width="1440" alt="Screenshot 2025-03-12 at 8 03 19 PM" src="https://github.com/user-attachments/assets/411fc8ea-5115-48cc-a8d1-bc55d9739790" />
</p>
<p>
 Congrats! You should see this screen and your osTicket should be set up and ready to go!
</p>
