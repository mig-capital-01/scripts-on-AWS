# scripts-on-AWS
All codes and scripts shared on AWS instances


### AWS set up

### launching and connecting to AWS EC2: https://medium.com/@praneeth.jm/launching-and-connecting-to-an-aws-ec2-instance-6678f660bbe6

### Install Python 3.6 and set it as default python version:
## sudo yum install python36

## alternatives --set python /usr/bin/python3.6
## python --version


### AWS EC2 Linux AMI with pyodbc, psqlODBC, Microsoft ODBC Drivers:

###  enable epel:

##  sudo yum-config-manager --enable epel epel-source epel-debuginfo #enable epel	 	
##  sudo yum repolist #verify epel was enabled Disable yum priority plugin
  
###  disable (annoying) yum priority plugin:
  
##  sudo nano /etc/yum/pluginconf.d/priorities.conf
  
##  enabled=0
  
###  Install Microsoft ODBC Driver 13.1 for SQL Server and unixODBC2.3x:
  
##  sudo su
##  curl https://packages.microsoft.com/config/rhel/6/prod.repo > /etc/yum.repos.d/mssql-release.repo
##  sudo ACCEPT_EULA=Y yum install msodbcsql
  
###  Install postgresql-odbc.x86_64:
  
##  sudo yum install postgresql-odbc.x86_64
  
###  Install pyodbc:
  
##  sudo yum install gcc-c++
##  sudo yum install python-devel
##  sudo yum install unixODBC-devel
##  sudo pip install pyodbc
  
###  Make sure security groups are appropriately configured for your MSSQL and PostgreSQL databases 
###  (IPV4 address for EC2 instances are added to Azure control group.)

### install pip:

## cd /tmp
## curl -O https://bootstrap.pypa.io/get-pip.py
## python3 get-pip.py --user
## pip --version

### install selenium (other packages that could be installed via pip):

## pip install selenium --user
  

### copy them from my local machine into the home folder of the ec2 instance:
## scp -i D:/ec2/test.pem D:/ec2/test.py ec2-user@ec2-18-191-31-0.us-east-2.compute.amazonaws.com:/home/ec2-user



