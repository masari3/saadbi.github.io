---
layout: post
title: How change Local Remote Directory Git in Linux System
description: How change Local Remote Directory Git in Linux System
color: 212121
author: masfitri
---
بسم الله الرحمن الرحيم
Title: Reconfig remote git directory<br/>
Level: Beginner<br/>
Refrence:<br/>
	- `http://google.com/`<br/>
	- `https://stackoverflow.com/questions/10904339/github-fatal-remote-origin-already-exists`<br/>
Purpose: <br/>
`Expected to be able to replace the git remote directory via linux terminal independently`<br/>

## Problem
{% highlight bash %}
	fatal: '/home/saadbi/Dropbox/git/appipos.git/' does not appear to be a git repository
	fatal: Could not read from remote repository.

	Please make sure you have the correct access rights
	and the repository exists.
{% endhighlight %}

## Suggested solution

1. Open Terminal
2. Change the shell working directory
	`cd ~/Dropbox/git/[project]`
3. Change remote git directory
	`git remote set-url origin ~/Dropbox/git/myproject.git/`
4. Try to push your git project
	`git push`
5. The result must be
	`Everything up-to-date`
6. Until this step the problem should have been solved!
	`Done`

الحمد لله
