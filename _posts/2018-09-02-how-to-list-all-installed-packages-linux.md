---
layout: post
title: How to list all installed packages in Linux (ubuntu)
description: How to list all installed packages in Linux (ubuntu)
color: B0360C
author: masfitri
---
بسم الله الرحمن الرحيم
<br/><br/>
#### Title: 
`Get a list of packages installed locally`<br/>

#### Level: 
`Beginner`<br/>

#### Refrence:
- `http://google.com/`<br/>
- `https://askubuntu.com/questions/17823/how-to-list-all-installed-packages`

#### Purpose:
`I'd like to output a list of all installed packages into a text file so that I can review it and bulk-install on another system. How would I do this?`

#### Suggested solution
##### Ubuntu 14.04 and above
The apt tool on Ubuntu 14.04 and above makes this very easy.
`apt list --installed`

##### Older Versions
To get a list of packages installed locally do this in your terminal:<br/>
`dpkg --get-selections | grep -v deinstall`

(The -v tag "inverts" grep to return non-matching lines).
To get a list of a specific package installed:<br/>
`dpkg --get-selections | grep postgres`


To save that list to a text file called packages on your desktop do this in your terminal:<br/>
`dpkg --get-selections | grep -v deinstall > ~/Desktop/packages`
Alternatively, simply use<br/>
`dpkg -l`
(you don't need to run any of these commands as the superuser, so no sudo or any other variants necessary here)

الحمد لله
