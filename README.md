## Nginx Web Hosting on Ubuntu EC2 Instance with HTTPS and Free SSL Certificate
###Project Overview
The objective of this project is to provision a server and deploy a prototype web application featuring a simple yet professional landing page. This landing page demonstrates the team's technical capabilities and vision, serving as a tool to attract potential investors. The project showcases proficiency in server setup, web development, and design by delivering a functional and visually appealing preview of the application.

## Step-by-Step Documentation: Server Provisioning and Deployment
1. Creating the Web Page
Designed a simple HTML page with minimal CSS for styling using Visual Studio Code.
Focused on clean and professional design while keeping the implementation lightweight.
2. Provisioning the Server
Utilized AWS EC2 to create a virtual server instance:
Assigned an instance name, generated a key pair, and created a security group.
Configured the security group to allow HTTP traffic (port 80).
After the instance was launched, connected to the server using SSH through the Termius terminal.
3. Installing and Configuring Nginx
Installed Nginx on the server with the following commands:
bash
Copy code
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
Verified the installation by visiting the server's public IP address in a browser, ensuring the default Nginx page was visible.
4. Transferring Project Files
Used WinSCP, a file transfer software, to upload the project folder (cloudproject) to the server.
Copied the project files to Nginx's root directory with:
bash
Copy code
sudo cp -r ~/cloudproject/* /var/www/html/
Verified that all files were copied correctly by listing the contents of the root directory:
bash
Copy code
ls -l /var/www/html
5. Running the Web Page
Refreshed the browser using the public IP address to display the deployed landing page.
IP Address
The project is accessible at 107.23.16.143 (temporary, for verification purposes only).

