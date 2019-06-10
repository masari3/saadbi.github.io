---
layout: post
title: Documentation
description: How change Local Remote Directory Git in Linux System
color: 212121
author: masfitri
---

## How change Local Remote Directory Git in Linux System
```
بسم الله الرحمن الرحيم
```
* Title: </br>`Reconfig remote git directory`
* Level: </br>`Beginner`
* Refrence: </br>
	- `http://google.com/` </br>
	- `https://stackoverflow.com/questions/10904339/github-fatal-remote-origin-already-exists`
* Purpose:</br>`Expected to be able to replace the git remote directory via linux terminal independently`

## The Problem
```sh
	fatal: '/home/saadbi/Dropbox/git/appipos.git/' does not appear to be a git repository
	fatal: Could not read from remote repository.

	Please make sure you have the correct access rights
	and the repository exists.
```
## Suggested solution

1. Open Terminal
2. Change the shell working directory </br>
	`cd ~/Dropbox/git/[project]`
3. Change remote git directory </br>
	`git remote set-url origin ~/Dropbox/git/myproject.git/`
4. Try to push your git project </br>
	`git push`
5. The result must be </br>
	`Everything up-to-date`
6. Until this step the problem should have been solved! </br>
	`Done`

```
الحمد لله
```
