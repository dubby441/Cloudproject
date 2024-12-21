

# Nginx Web Hosting on Ubuntu EC2 Instance with HTTPS and Free SSL Certificate

## Project Overview

The objective of this project is to provision a server and deploy a prototype web application featuring a simple yet professional landing page. This landing page demonstrates the team's technical capabilities and vision, serving as a tool to attract potential investors. The project showcases proficiency in server setup, web development, and design by delivering a functional and visually appealing preview of the application.

---

## Repository Highlights

This repository provides a comprehensive guide to:  
✅ Setting up an Ubuntu EC2 instance for web hosting.  
✅ Installing and configuring Nginx to serve your web content.  
✅ Securing your website with HTTPS using a free SSL certificate from Let’s Encrypt.  
✅ Deploying a custom domain with professional configurations.  

Designed to go beyond a basic tutorial, this project serves as a complete toolkit for creating a secure, scalable, and reliable web server aligned with modern web standards. Whether you're new to web hosting or an experienced developer, this repository will enhance your skills and deepen your understanding of hosting and web security.

---

## Prerequisites  

Before starting, ensure you meet the following requirements for a smooth experience:  

- 🔧 **Basic Linux Command Skills**: Familiarity with essential Linux commands will help you navigate and manage the server effectively.  
- ☁️ **EC2 Instance Setup**: Understanding how to launch an EC2 instance and configure security groups for HTTP and HTTPS traffic.  
- 💻 **Development Environment**: Tools like Git Bash or Visual Studio Code (VSCode) for managing files and running commands.  

With these prerequisites in place, you’re all set to dive in! 🚀  

---

## Step-by-Step Documentation: Server Provisioning and Deployment  

### 1. **Creating the Web Page**  
- Designed a simple HTML page with minimal CSS for styling using Visual Studio Code.  
- Focused on clean and professional design while keeping the implementation lightweight.  

### 2. **Provisioning the Server**  
- Utilized **AWS EC2** to create a virtual server instance:  
  - Assigned an instance name, generated a key pair, and created a security group.  
  - Configured the security group to allow **HTTP traffic** (port 80).  
- After launching the instance, connected to the server using **SSH** through the **Termius** terminal.  

### 3. **Installing and Configuring Nginx**  
- Installed Nginx on the server with the following commands:  
  ```bash
  sudo apt update
  sudo apt install nginx -y
  sudo systemctl start nginx
  sudo systemctl enable nginx
  ```  
- Verified the installation by visiting the server's public IP address in a browser to confirm the default Nginx page was displayed.  

### 4. **Transferring Project Files**  
- Used **WinSCP**, a file transfer software, to upload the project folder (`cloudproject`) to the server manually. However, the command below also works:
- Copied the project files to Nginx's root directory with:  
  ```bash
  sudo cp -r ~/cloudproject/* /var/www/html/
  ```  
- Verified the file transfer by listing the contents of the root directory:  
  ```bash
  ls -l /var/www/html
  ```  

### 5. **Enabling HTTPS with Let’s Encrypt**  
- Installed the required packages for managing SSL certificates:  
  ```bash
  sudo apt update
  sudo apt install certbot python3-certbot-nginx -y
  ```  
- Obtained and installed a free SSL certificate for the domain `dubem.web.jumpingcrab.com`:  
  ```bash
  sudo certbot --nginx -d dubem.web.jumpingcrab.com
  ```  
  This command automatically configured the Nginx server to enable HTTPS.  

### 6. **Verifying the SSL Certificate**  
- Verified the SSL certificate by visiting [https://dubem.web.jumpingcrab.com](https://dubem.web.jumpingcrab.com).  
- Ensured the secure connection was active by checking for the padlock icon in the browser’s address bar.  

### 7. **Running the Web Page**  
- Refreshed the browser using the public IP address or domain to display the deployed landing page.  

---

## IP Address  

The project is accessible temporarily at **[107.23.16.143](http://107.23.16.143)** for verification purposes only.  
