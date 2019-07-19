---
layout: post
title: How change Local Remote Directory Git in Linux System
description: How change Local Remote Directory Git in Linux System
color: BF360C
author: masfitri
---
بسم الله الرحمن الرحيم
<br/><br/>
### Title: 
`Reconfig remote git directory`<br/>

### Level: 
`Beginner`<br/>

### Refrence:
- `http://google.com/`<br/>
- `https://stackoverflow.com/questions/10904339/github-fatal-remote-origin-already-exists`

### Purpose:
`Expected to be able to replace the git remote directory via linux terminal independently`

### Problem
{% highlight yml %}
fatal: '/home/saadbi/Dropbox/git/appipos.git/' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
{% endhighlight %}

### Suggested solution
1. Open Terminal
2. Change the shell working directory<br/>
	`cd ~/Dropbox/git/[project]`
3. Change remote git directory<br/>
	`git remote set-url origin ~/Dropbox/git/myproject.git/`
4. Try to push your git project<br/>
	`git push`
5. The result must be<br/>
	`Everything up-to-date`
6. Until this step the problem should have been solved!<br/>
	`Done`

الحمد لله
