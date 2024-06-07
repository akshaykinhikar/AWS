# AWS

### Start script for aws

```
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1> Hello world from $(hostname -f)</h1>" /var/www/html/index.html
```

### Create instance and save `Key pair (login)` in a folder 
```
ssh ec2-user@****PUBLIC IP ADDRESS****

```
### you might get 
```
ec2-user@51.20.133.54: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
```

### try
```
ssh -i SecondInstance.pem ec2-user@51.20.133.54
```
```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0664 for 'SecondInstance.pem' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "SecondInstance.pem": bad permissions
ec2-user@51.20.133.54: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
```

### change permision and connect again 
```
chmod 0400 SecondInstance.pem
ssh -i SecondInstance.pem ec2-user@**** PUBLIC IP ****
```
### connected successfully
```
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-172-***-**-** ~]$ 
```

### Disconnect `ctrl + d`


