---
layout: post
title: Can't install mysql on centos 7
description: install yum repos as mentioned here on installing mariadb instead of mysql
color: 30dfcd
author: masfitri
---

بسم الله الرحمن الرحيم
<br/><br/>
### Title
Install MySQL version 5.7 in Centos 7.x DigitalOcean

### Level: 
`Beginner`<br/>

### Refrence:
- `https://www.digitalocean.com/community/questions/can-t-install-mysql-on-centos7-2` <br/>

### Purpose:
`It looks like you have missed installing the required RPMs. Please give a try to below steps:`

### Suggested solution

1. Install wget, by default vm / vps not installed<br/>
`yum install wget -y`

2. Download MySql repository<br/>
`wget https://dev.mysql.com/get/mysql57-community-release-el7-9.noarch.rpm`

3. Verify the md5sum of file<br/>
`md5sum mysql57-community-release-el7-9.noarch.rpm`

4. Install RPM file<br/>
`rpm -ivh mysql57-community-release-el7-9.noarch.rpm`

5. Install mysql server with this command<br/>
`yum install mysql-server -y`


### Note:
Dont forget if we not in sudo user or root user.
