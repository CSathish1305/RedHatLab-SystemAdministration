# RedHatLab-SystemAdministration ( RHCSA EXAM SYLLABUS )
- GOAL : To Learn and Gain Hands On Experience on the Basics of System Administration using Red Hat OS ( Using RHCSA Syllabus )
# System Administration Tasks 
# 1.Understanding & Use Essential Tools
  - Create file Using Touch, Copy, Vim Editor, Nano Editor.
    ![Screenshot 2024-12-18 132418](https://github.com/user-attachments/assets/0ff6ec3e-4c30-4642-be53-5dd9b32f998a)
    ![Screenshot 2024-12-18 132737](https://github.com/user-attachments/assets/55f52ace-6a1f-4b67-81da-b521795c21b4)
    ![Screenshot 2024-12-18 132809](https://github.com/user-attachments/assets/74666cac-7096-4f7d-9963-8a1d487c182a)
    ![Screenshot 2024-12-18 133246](https://github.com/user-attachments/assets/f5589c42-d8dc-45de-a68a-fd0b06449979)
    ![Screenshot 2024-12-18 133427](https://github.com/user-attachments/assets/753aac9b-d815-4a6b-a492-66742f82cf65)
  - Redirect the Output using >, >>, |, 2> Symbols
    ![Screenshot 2024-12-28 180801](https://github.com/user-attachments/assets/0b70f65f-ba66-4e23-9c03-92654e72892a)
  - Remove the files using rm command
    ![image](https://github.com/user-attachments/assets/37447fe1-fda1-442c-a314-7f2afc201c1c)
  - Search keywords in a file and directories Using Grep 
    ![Screenshot 2024-12-18 131019](https://github.com/user-attachments/assets/72922626-b62d-4335-b346-fbd5d95b7589)
  - Sorting Data of a file usig sort command {OPTIONS: '-r' -> reverse, '-n' -> By num, '-f' -> Ignore case, '-u' -> without duplicates}
    <img width="960" alt="image" src="https://github.com/user-attachments/assets/a7ec316d-f17b-418f-bd3b-9ae960be430f" />
  - Remote login using SSH with keys
    ![Screenshot 2024-12-30 140655](https://github.com/user-attachments/assets/89892485-6eab-4acb-96b4-663cf3cc293d)
    ![Screenshot 2024-12-30 210452](https://github.com/user-attachments/assets/30ef00aa-71ac-47f1-9b8c-b7a12b7074dd)
    ![Screenshot 2024-12-30 210600](https://github.com/user-attachments/assets/9745ca3d-f4bd-4345-a90b-bbb1d05a192c)
  - File Transfer using SCP(Secure Copy Protocol)
    ![Screenshot 2024-12-30 222131](https://github.com/user-attachments/assets/3e3e090a-d6d7-46e8-80ce-9b0b643679c8)
    ![Screenshot 2024-12-30 222226](https://github.com/user-attachments/assets/c28e2df2-025b-49ab-a4c6-d8a890f733a5)
  - Login & Switch Users :
    $ sudo systemctl isolate multi-user.target
  - To make the user default on boot :
    $ sudo systemctl set-default multi-user.target
  - To switch to a Graphical target :
    $ sudo systemctl isolate graphical.target
  - To list available targets
    $ sudo systemctl list-unit --type=target
  - Check Current Target
    $ sudo systemctl get-default
  - To list logged users :
    $ who
    $ w
  - To kill a User Session :
    $ sudo pkill -u [username]
  - Understanding File Permissions
    ![Screenshot 2024-12-18 165340](https://github.com/user-attachments/assets/a9f6e2de-aa07-44bc-b79a-385a7ce503b2)
  - Changing File Permissions for Users, Groups, Owners using Chmod command 
    ![Screenshot 2024-12-18 170129](https://github.com/user-attachments/assets/7bcd1330-5dd0-419c-94d3-2efbbef5f5bf)

# 2.Operate Running Systems 
  - Boot the system--> If the system is powered off, start it using the power button.Red Hat systems typically use systemd as the init system to manage booting.
  - Reboot the system : $ reboot (use sudo if needed)
  - Shutdown a system Manually : $ poweroff or shutdown now (use sudo if needed)
  - Monitoring Processes using ps command
    ![Screenshot 2024-12-18 170406](https://github.com/user-attachments/assets/4eb87ca4-24ee-408d-9757-b4cf73f84f4b)
  - Realtime Process Monitoring using top
    ![Screenshot 2024-12-18 170432](https://github.com/user-attachments/assets/70693b78-9dde-4b86-918b-d0c1bc57395a)
  - Identify CPU/memory intensive processes and kill processes
    ![image](https://github.com/user-attachments/assets/d234d3b3-cc5d-4edc-a379-34c56a1052c6)
    View Log Files
  - Logs are stored in /var/log. Common files include:
    /var/log/messages (general system messages)
    /var/log/secure (authentication logs)
    /var/log/dmesg (kernel ring buffer)
  - Read logs : $ sudo less /var/log/messages
  - Use journalctl to view logs:
    View Recent Logs : $ journalctl -n 50
    View Specific Logs : $ Journalctl -u < service_name >
  - Start, Stop, and Check the Status of Network Services
    ![image](https://github.com/user-attachments/assets/6fee70d3-2b36-49d3-9d41-55e9570bd24b)
 
# 2.Manage Basic Networking 
  - Checking Network connection to the outside network using Ping command
    ![Screenshot 2024-12-18 135704](https://github.com/user-attachments/assets/7e54f4fc-b747-4135-8070-9253e9ae4be1)
  - Checking the path or route the packets take to reach a destination using tracert
    <img width="428" alt="Screenshot 2024-12-18 161536" src="https://github.com/user-attachments/assets/89ce90cf-089d-4bfa-b0bc-3c68ec827ad7" />
  - Displays active network connections and listening ports using Netstat command and ss command & Display ARP Table using arp command (NOTE: ss is the modern version of netstat with faster output)
  ![Screenshot 2024-12-18 153209](https://github.com/user-attachments/assets/bec6c38a-483b-4652-9cb2-36a369fa96c6)

  - Checking DNS using nslookup & Checking ports of a host using telnet
  - ![Screenshot 2024-12-18 152629](https://github.com/user-attachments/assets/8dee90df-64bc-41ac-ace5-149293defe47)
  - Capture packets and store it in a file using tcpdump command 
  ![Screenshot 2024-12-18 142654](https://github.com/user-attachments/assets/088db9ae-b497-4cc4-84b7-eacb3264933b)
  
# 3.Configure local storage

# 3.Adding & Removing softwares
  - Managing Packages & Using rpm to list all packages available
    ![image](https://github.com/user-attachments/assets/c337eba0-fa4c-4b73-a9fd-fa7c38cd0f63)
  - Show Package Info
    ![Screenshot 2024-12-18 163855](https://github.com/user-attachments/assets/2132090a-8b39-4a21-b973-b44cf36b2716)
  - Install New Package!
    ![Screenshot 2024-12-18 164118](https://github.com/user-attachments/assets/68af0c7e-97b3-4eaf-bc09-dde10066bb9c)
  - Remove Package
    ![image](https://github.com/user-attachments/assets/3fb14008-7ade-4545-ada7-fb9be00f3aaf)


 
# 6.Managing User Environment variables
  - Using Environment Variables
  - Setting Local Environment Variables
  - Setting Global Environment Variables
# 7.Compressing & Archiving 
  - Compress Data
# 8.Filesystem & Storage Device Management 
  - Monitoring Disk Space using Df and Du Commands
    ![Screenshot 2024-12-18 172752](https://github.com/user-attachments/assets/26d89f72-d088-4464-861a-9dc4076ebdd1)
# 9.User & Group Management
  - Using Useradd & Userdel Commands Create a User & Delete the User 
    ![image](https://github.com/user-attachments/assets/f19076a0-4b80-4fbf-93c4-ceae000aca6f)
  - Locking and Unlocking User Accounts
  - Understanding Groups, Creating Groups, Modify Groups, Delete Groups

# Server Administration Tasks

# 1.Installing Web Server 
  - Installing Apache Server
  - Modifying Apache Server Home Page
  - Monitor Apache Error Logs
# 2.Firewall
  - Understanding Firewall
  - Configuring Firewall Rules
# 3.Installing PHP 
  -  Installing PHP
  -  Links
  -  Test PHP on Apacher Server
# 4. Installing MySQL Database
  - Installing MySQL Package
  - Configuring MySQL Server
  - Working with MySQL Commands
  - Using MySQL in PHP
  - Fixing Issue and Testing the Script
