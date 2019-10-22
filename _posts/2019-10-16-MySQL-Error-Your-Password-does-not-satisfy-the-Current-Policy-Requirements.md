---
layout: post
title: MySQL Error : "Your Password does not satisfy the Current Policy Requirements"
description: Error Your Password does not satisfy the Current Policy Requirements
color: cdcdcd
author: masfitri
---

بسم الله الرحمن الرحيم
<br/><br/>
### Title
MySQL Error : "Your Password does not satisfy the Current Policy Requirements"

### Level: 
`Beginner`<br/>

### Refrence:
- `https://hoststud.com/resources/resolved-mysql-error-your-password-does-not-satisfy-the-current-policy-requirements.464/` <br/>
- `https://dev.mysql.com/doc/refman/5.6/en/validate-password-options-variables.html`

### Purpose:
`Default Password level of plugin can be changed at runtime or using config file. To do this, default authentication plugin has to be checked.`

### Suggested solution

`SHOW VARIABLES LIKE 'validate_password%';`
`SET GLOBAL validate_password_policy=LOW;`
`validate_password_policy=LOW`
`sudo service mysqld restart`

Uninstall Plugin used for Password Validation
`mysql -u root –p`
`UNINSTALL PLUGIN validate_password;`
