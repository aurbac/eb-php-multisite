# PHP Multisite with AWS Elastic Beanstalk

## VPC with Public and Private subnets required

CloudFormation Template: [VPC-Public-And-Private](https://raw.githubusercontent.com/aurbac/msg-app-backend/master/vpc/AURBAC-VPC-Public-And-Private.json)

Replace values in **.ebextensions/vpc.config** with the resources created by the CloudFormation template.

## Clone Github Project

``` bash
git clone https://github.com/aurbac/eb-php-multisite.git
cd eb-php-multisite
```

## Change Virtual Hosts for your Apache server

Edit the file **.ebextensions/vhosts.config** with your own domains.

## Initialize Elastic Beanstalk Project

``` bash
eb init
```

Select a default region: **1) us-east-1 : US East (N. Virginia)**


Select an application to use: **1) sites**


It appears you are using PHP. Is this correct? **Y**


Select a platform version. **3) PHP 7.0**


Do you want to set up SSH for your instances? **Y**


Select a keypair. **(Select your KeyPair)**

## Create your first Environment

``` bash
eb create
```

Enter Environment Name: **(default is sites-dev)**


Enter DNS CNAME prefix: **(default is sites-dev)**


Select a load balancer type: **2) application**


Wait a few minutes until your environment is deployed.