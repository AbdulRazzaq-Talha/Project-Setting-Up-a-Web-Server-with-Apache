# Project-Setting-Up-a-Web-Server-with-Apache

**Introduction**
This project involves setting up a web server using Apache on Oracle VM VirtualBox. 
The steps include installing necessary packages, configuring the server, and ensuring it is operational.

**Steps**

**1: Install YUM Package Manager**
Ensure YUM is installed and updated on your virtual machine.
YUM is a package manager that simplifies the process of installing and managing software packages
Command : **sudo yum update**
Result: ![image](https://github.com/user-attachments/assets/cc27d914-0dc7-4561-8529-f26639198f14)

**2: Install Apache (httpd)**
Install Apache, a widely-used web server software, using the YUM package manager.
Command: sudo yum install httpd
Result: ![image](https://github.com/user-attachments/assets/f1719de7-4eb8-45c7-9e9c-1cf0f08d1c33)

**3: Enable/Start and Verify Apache Service**
Enable the Apache service to start on boot and then start the service.
Command : sudo systemctl enable httpd
          sudo systemctl start httpd
          sudo systemctl status httpd
Result: ![image](https://github.com/user-attachments/assets/adb4a5f4-53b5-4185-9d6d-0269845c99a8)

****4: Configure Website Interface** / **Create and Save a Hyperlink**
Create and upload your website files to the appropriate directory.
The default directory for Apache web files is /var/www/html/.
Create an HTML file with a hyperlink and save it in the appropriate directory.
Command : sudo cp /path/to/your/website/files /var/www/html/

**5: Configure Firewall**
Add firewall rules to allow HTTP traffic, ensuring that the web server can be accessed from outside the virtual machine.
Command : sudo firewall-cmd --permanent --add-service=http
          sudo firewall-cmd --reload
Results: ![firewall settings](https://github.com/user-attachments/assets/c177af85-fb4f-4a10-b0fa-7391cf3ea853)

          
**6: Verify Website Functionality**
Open a web browser and navigate to your server’s IP address to confirm the website is working. 
You should see your website’s homepage if everything is set up correctly.
Results:![website launched for apache](https://github.com/user-attachments/assets/48090fb6-c979-4c08-a4b9-edf1c7cb1f10)

