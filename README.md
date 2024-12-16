# Cloudproject
The goal of this project is to develop a prototype for a web application by provisioning a server and deploying a simple yet professional landing page. The landing page will serve as a demonstration of the team's technical capabilities and vision, aiming to attract potential investors. The project focuses on showcasing a functional and visually appealing preview of the application, highlighting the team's proficiency in server setup, web development, and design.

## Step-by-step documentation on how the server was provisioned
Firstly, a simple HTML page was created and little css was added to the code to make it look better using the VS code, nothing too technical.
Secondly, using AWS an instance was created which involves creating an instance name, keypair and a security group which was configured to allow HTTP traffic(port 80).
Furthermore, after the server was created, the command line(Termius) was used to connect to the server using SSH and once the server was able to be accessed through the command line, ngnix was installed using the code "sudo apt install nginx" then followed by starting it with the code "sudo systemctl start nginx" and enabling it with "sudo systemctl enable nginx". Note: After running this code, the public ip was copied and pasted on the browser to see if the ngnix was visible.
Consequently, Winscp (this is a software for file transfer) was downloaded and the project folder was sent to the web server in order to get the webpage up and running on the browser. After doing that, the folder was copied to the ngnix root directory with the code, "sudo cp -r ~/cloudproject/* /var/www/html/" and to be sure every was copied correctly, another command was run which is, " ls -l /var/www/html" to list all the files in the root directory.
Finally, after getting everything right, you refresh the ip address that was copied earlier on your browser for your webpage to run.

## IP Address
The ip address (107.23.16.143) is solely for the purpose of verification and would be removed after it has been verified.
