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
<p><img width="624" alt="Screenshot 2025-03-03 at 10 49 31 AM" src="https://github.com/user-attachments/assets/ffde316e-a3d4-401e-ba66-ecb19ac8de8f" />
</p>
<p><img width="608" alt="Screenshot 2025-03-03 at 10 52 57 AM" src="https://github.com/user-attachments/assets/264d6738-54d0-490e-b73c-e53e215e0271" />
</p>
<p>
  Here, we are setting up the mySQL database that will be needed for our ticketing system. It is important to remember the log in information that we would have set up earlier in the insall. 
</p>

<br />

<p><img width="1440" alt="Screenshot 2025-03-01 at 2 42 10 PM" src="https://github.com/user-attachments/assets/3e363955-49bc-4928-9d19-84035a4c5d06" />
</p>
<p>
  After getting all files downloaded and configured, we are able to run osTicket. There are still a few extensions that we will configure through IIS and PHP Manager. 
</p>
<br>
