---
layout: post
title: How to install different php 5.x and php 7.x on Ubuntu 18.04 LTS
description: Switchable php version on ubuntu
color: 39ddcd
author: masfitri
---

بسم الله الرحمن الرحيم
<br/><br/>
### Title
How to install different php 5.x and php 7.x on Ubuntu 18.04 LTS

### Level: 
`Beginner`<br/>

### Refrence:
- `https://vitux.com/how-to-install-php5-and-php7-on-ubuntu-18-04-lts/` <br/>
- `https://www.tecmint.com/install-different-php-versions-in-ubuntu/` <br/>
- `google.com`

### Purpose:
`Easy command how to change php version, because old project using old version php.`

### Suggested solution
1. Add repository sourcelist for php5xxx with this command in your beautiful terminal <br/>
`sudo add-apt-repository ppa:ondrej/php`

2. If our ubuntu not automatic Update, run manual update 
`sudo apt update`

3. Install php 5 then install php 7, we can type one line command like this  <br/>
`sudo install php5.6 && sudo install php7.2`

4. After instalation geting finish, check default php <br/>
`sudo update-alternative --config php`

5. how to enable php 5 ? <br/>
step one: `sudo a2dismod php7.2`  <br/>
step two: `sudo a2enmod php5.6`

6. how to enable php 7
step one: `sudo a2dismod php5.6`  <br/>
step two: `sudo a2enmod php7.2`
