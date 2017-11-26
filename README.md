# LinuxServer
### Udacity Full Stack Web Developer Nanodegree Project

#### A Project to take a baseline installation of a Linux distribution on a virtual machine and prepare it to host your web applications, to include installing updates, securing it from a number of attack vectors and installing/configuring web and database servers.

#### i. IP Address and SSH Port
1. IP Address: 34.199.98.221
2. SSH Port: 2200

#### ii. Application URL
1. http://34.199.98.221.xip.io

#### iii. Summary of software installed and configuration made
1. Set local timezone to UTC using sudo dpkg-reconfigure tzdata command
2. Changed the default ssh port to 2200 by editing /etc/ssh/sshd_config
3. Using ufw, firewall is set to only allow access from port 80(www), port 2200(ssh), and port 123(ntp)
4. Created new user named grader using adduser command
5. Gave sudo permission to grader by creating file in /etc/sudoers.d/grader containing the sudo permissions
6. Generate SSH Key Pair for grader using ssh-keygen from my machine
7. Put the ssh public key inside the grader .ssh/authorized_keys file
8. Install apache2 web server using sudo apt-get install apache2
9. Install mod_wsgi for python 3 using sudo apt-get install libapache2-mod-wsgi-py3
10. Install Postgresql using sudo apt-get install postgresql
11. Setup postgresql by creating catalog user and catalog database
12. Create initial table using python script from catalog project
13. Populate initial data using python script from catalog project
12. Configure apache2 config in /etc/apache2/sites-available/000-default.conf to allow access to flask web app in /var/www/Catalog/catalog.wsgi
13. Create file in /var/www/Catalog/catalog.wsgi that setup the application inside the Catalog directory
14. Copy catalog app to /var/www/Catalog/Catalog
15. Restart apache2 webserver

#### iv. Third party resources
https://digitalocean.com - Deploy Flask on Ubuntu, Configure Postgresql, change default ssh port