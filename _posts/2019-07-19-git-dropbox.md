---
layout: post
title: Local Remote Directory Git in GNU/Linux System
description: Local Remote Directory Git in GNU/Linux System
color: BF360C
author: masfitri
---


<br/><br/>
## Title: 
### Reconfig remote git directory<br/>

## Level: 
### Beginner<br/>

## Refrence:
`jetheis.com/blog/2013/02/17/using-dropbox-as-a-private-github/`
`google.com`

## Purpose:
`An easy solution to starting Git with Dropbox, hosting free, powerful files.`
{% highlight yml %}
$ cd ~/Dropbox/Git
$ git init --bare mytestrepo.git
  Initialized empty Git repository in /home/abdullah/Dropbox/Git/mytestrepo.git/
  
$ cd ~
$ mkdir testrepo
$ cd testrepo
$ git init
  Initialized empty Git repository in /home/jetheis/testrepo/.git/
$ echo "Some Text" > testfile.txt
$ git add testfile.txt
$ git commit -m "Add a test file"
  [master (root-commit) 0220f05] Add a test file
   1 file changed, 1 insertion(+)
   create mode 100644 testfile.txt
$ echo "More text" >> testfile.txt
$ git commit testfile.txt -m "Add more text"
  [master f014b59] Add more text
   1 file changed, 1 insertion(+)

$ git remote add origin ~/Dropbox/Git/mytestrepo.git

$ git push -u origin master
  Counting objects: 6, done.
  Delta compression using up to 4 threads.
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (6/6), 458 bytes, done.
  Total 6 (delta 0), reused 0 (delta 0)
  Unpacking objects: 100% (6/6), done.
  To /Users/jetheis/Dropbox/Git/mytestrepo.git
   * [new branch]      master -> master
  Branch master set up to track remote branch master from origin.
{% endhighlight %}
