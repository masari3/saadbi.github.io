---
layout: post
title: Local Remote Directory Git in GNU/Linux System
description: Local Remote Directory Git in GNU/Linux System
color: BF360C
author: masfitri
---

بسم الله الرحمن الرحيم
<br/><br/>
## Title: 
### Local Git Remote Directory to Dropbox<br/>

## Level: 
### Beginner<br/>

## Refrence:
`jetheis.com/blog/2013/02/17/using-dropbox-as-a-private-github/` <br/>
`google.com`


## Purpose:
`An easy solution to starting Git with Dropbox, hosting free, powerful files.`


## Solution
1. Open your favorite terminal
2. Change to work directory<br/>
	`$ cd ~/Dropbox/Git`
3. Make directory with extension .git<br/>
	`$ mkdir myapp.git` 
4. Type this command and hit enter<br/>

5. Create an empty Git repository or reinitialize an existing one<br/>
	`$ git init --bare myapp.git`

6. Move to your directory project ex:<br/>
	`$ cd ~/www/myapp/`

7. Initialize an existing one with the command<br/>
	`$ git init .`

8. Create some file ex: myfile.txt<br/>
	`$ echo "My First Files with Versioning Control Git Local to Dropbox Folder " > myfile.txt`
	
9. Add your file to versioning control with command<br/>
	`$ git add myfile.txt`
	
10. Commit the file after done creating or editing<br/>
	`$ git commit -m "my file version 1.0"`
{% highlight yml %}
[master (root-commit) 0220f05] Add a test file
1 file changed, 1 insertion(+)
create mode 100644 myfile.txt
{% endhighlight %}
	
11. Remote local to dropbox folder<br/>
	`$ git remote add origin ~/Dropbox/Git/myapp.git`
	
12. Push to dropbox<br/>
	`$ git push -u origin master`
{% highlight yml %}
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 458 bytes, done.
Total 6 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (6/6), done.
To /home/abdullah/Dropbox/Git/myapp.git
* [new branch]      master -> master
Branch master set up to track remote branch master from origin.
{% endhighlight %}