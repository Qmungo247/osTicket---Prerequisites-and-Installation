# osTicket-Prerequisites-and-Installation

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
An outline of the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Download OsTicket Installation Files Software
- Installation/Enable Internet Information Services (IIS) in Windows with CGI.
  A web server that runs Osticket on the PC. 
- Installation off PHP Manager for IIS (Backend web server language/Binary. requirement to run OsTicket)
- Installation of VC Redist & MySQL Database (Backend data storage)
- Item 5
<h2>Installation Steps</h2>

<p>

  ![Screenshot 2024-09-24 163156](https://github.com/user-attachments/assets/5d141eb2-6812-4bca-8717-d6f3bdbf8892)

![Screenshot 2024-09-25 142538](https://github.com/user-attachments/assets/8f2966ab-8e1d-4b15-9bad-267ca64218e5)


</p>
<p>
After Downloading & Installing the OsTicket files software. You want to enable Internet Information Services & CGI in the control panel of the PC. 
Control Panel > Programs > Programs & Features > Click "Turn Windows Features on or off" Link on the left hand side. Scroll down to & check "Internet Information Services".
Then expand the folder > Expand "World Wide web services" folder > Expand "Application Development Features" Folder > Check CGI then click OK
  
</p>
<br />

<p>

  ![Screenshot 2024-09-26 162305](https://github.com/user-attachments/assets/c9036462-bf00-4d72-89f4-02d9a358dcdd)

  ![Screenshot 2024-09-26 162826](https://github.com/user-attachments/assets/e6c66eb0-a41b-43e1-b5d9-d7ad28f6d789)

  ![Screenshot 2024-09-26 163019](https://github.com/user-attachments/assets/a04ab6ef-25aa-4d50-995e-9c34961d517e)



</p>
<p>
From the "OsTicket Installation Files" Folder downloaded in the frist step. Install PHP Manager for IIS & the Rewrite Module. Next, Create a New folder in the C: Drive of the PC & label it PHP. Then extract the PHP 7.3.8 folder found in the "OsTicket Installation Files" into the new PHP folder created in the C: Drive.
</p>
<br />

<p>

 ![Screenshot 2024-09-26 165459](https://github.com/user-attachments/assets/dac63c10-7a43-417b-951b-789a9332d302)

 ![Screenshot 2024-09-26 165544](https://github.com/user-attachments/assets/1ef9e6ab-a95b-48b4-81a9-ed7bbfd8a434)


</p>
<p>
From the "OsTicket Installation Files Folder Install "VC Redist" & "MySQL5.5.62" Typical Setup > Launch Configuration Wizard (after install) >
Standard Configuration > Next >  Username: root Password: root

</p>
<br />

<p>

![Screenshot 2024-09-26 193630](https://github.com/user-attachments/assets/d4b7236c-48d6-45c5-8170-6a02f463f044)

 ![Screenshot 2024-09-26 193735](https://github.com/user-attachments/assets/b9d672fc-16a0-42eb-aff1-9e22b749fc1f)

 ![Screenshot 2024-09-26 193751](https://github.com/user-attachments/assets/ba32f481-c572-4808-94e7-70c6f97925b0)

 ![Screenshot 2024-09-26 195055](https://github.com/user-attachments/assets/aeadb87f-e538-46bb-92e9-2879d00681c9)

 ![Screenshot 2024-09-26 195349](https://github.com/user-attachments/assets/b657b2e6-2b58-44c2-8c7d-d55b5c7a46ed)





</p>
<p>
Open IIS as admin from start menu & register PHP from within IIS (PHP Manager > C:\PHP\php-cgi.exe) > Next Reload ISS (Stop & Start the server)

  ![Screenshot 2024-10-02 170134](https://github.com/user-attachments/assets/74f35598-aff6-4b1e-9cf9-e487422cd1b9)


![Screenshot 2024-10-02 170926](https://github.com/user-attachments/assets/fb4d419f-7d77-4d35-9ae1-87d5c3f320a5)


  
  Next, Install/Extract all "osTicket v1.15.8" folder from the "osTicket-Installation-Files" folder. It should create a new folder with "Scripts" & "Upload" within it. 
  Then copy the "upload" folder into "C:\inetpub\wwwroot" & rename it "osTicket" Exactly with no space. Next Reload IIS Manager (Start & stop the server)

  ![Screenshot 2024-10-02 172033](https://github.com/user-attachments/assets/42f1ac46-8b7a-4541-906f-8f133d427796)

From within IIS Manager on the left Click "Sites" > Default Web Site > OsTicket then clcik "Browse *:80" on the right.
Go back to IIS, click sites -> Default -> osTicket. Double-click PHP Manager. Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes



</p>
<br />
