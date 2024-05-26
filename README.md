# LAMP STACK IMPLEMENTATION(PROJECT 1)

**A LAMP** Stack is a solution stack that is being used in deploying web applications. It stands for Linux, Apache, MySql and php,perl or python.

**Linux**: this is an operating system which serves as the backbone of the LAMP Stack, and it is actively used in deploying other components.

**Apache**: is a web server software which via HTTP requests processes requests and transmits information via the internet.

**MySQL**: use for creating and maintaining dynamic databases. It supports SQL and relational tables and provides a DBMS(Database Management System).

**PHP,PERL or PYTHON**: this represents programming languages which effectively combines all the elements of the LAMP stack and is used to make web applications execute.

### Creation of EC2 Instance

First we log on to AWS Cloud Services and create an EC2 Ubuntu VM instance. When creating an instance, choose keypair authentication and download `private key(*.pem)` on your local computer.

![alt text](images/1.1.png)

On windows terminal, `cd` into the directory containing the downloaded private key.Run the below command to log into the instance via ssh:

![alt text](images/1.2.png)

successful login to instance

### Setting Up Apache Web Server

To deploying the web application, we need to install apache via ubuntu package manager `apt`:

```
#Updating Packages
$ sudo apt update

$ sudo apt install apache2
```

![alt text](images/1.3.png)

```
#starting apache2 Server
$ systemctl start apache2

#ensuring apache2 starts automatically on system boot
$ systemctl enable apache2

#checking server spunned
$ systemctl status apache2
```

![alt text](images/1.4.png)

If it shows a green text, it means the web server has been successfully spunned and is live.
