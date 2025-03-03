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

<p><img width="1440" alt="VM-OSticket" src="https://github.com/user-attachments/assets/6ba89019-0c7b-4e4d-aa8b-7211588dd232" />
 
</p>
<p>
After getting our Windows 10 VM running in Azure, we need to download the files necessary to run our ticketing system. I will install the necessary files which will not only setup osTicket, but also our database through mySQL/HeidiSQL, and help us configure IIS. 
</p>
<br />

<p><img width="1440" alt="Screenshot 2025-03-01 at 1 28 27 PM" src="https://github.com/user-attachments/assets/5a86ac97-806f-458c-8778-4f5cd257a67d" />

    
</p>
<p>
While downloading the necessary files, we are slowly able to configure Internet Information Services. This will help us to run osTicket and configure necessary extensions through PHP/PHP Manager.  
</p>
<br />

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
