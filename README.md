# active-directory-project
A project showcasing Active Directory setup using Windows Server 2019, Windows 10 VM-ware.



This project includes a PowerShell script (1_CREATE_USERS.ps1) that automates the creation of Active Directory users from a plain text file (names.txt).

📂 File Structure
1_CREATE_USERS.ps1: Main PowerShell script that creates users in Active Directory.
names.txt: A text file with one full name per line (e.g., John Doe, Jane Smith).
⚙️ How It Works
Read Names:
The script reads each line from names.txt, which should contain full names (First Last).
Parse Name:
Each name is split into FirstName and LastName.
Generate Username:
The username is generated using the first initial and last name, all lowercase (e.g., jdoe).
Generate Password:
The password is set to FirstName123! and marked for change at first login.
Create User:
A new Active Directory user is created with the specified SamAccountName, UserPrincipalName, and password.
User Login Info:
Example for John Doe:
Username: jdoe
Password: John123!
UPN: jdoe@yourdomain.com
🛠️ Requirements
Active Directory module for PowerShell
Domain permissions to create users
A valid domain name (update yourdomain.com in the script)
