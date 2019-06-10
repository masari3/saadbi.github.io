## No space left on device (ENOSPC) when starting mkdocs
```
بسم الله الرحمن الرحيم
```

* Title: </br>`Errno=No space left on device (ENOSPC)`
* Level: </br>`Beginner`
* Refrence: </br>
	- `https://github.com/edx/configuration/issues/4015`
* Purpose: </br>
`Run the mkdocs application without error messages`

### The Problem
```sh
	...
	[2018-12-08 21:33:54,013 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/themes/mkdocs/css WD=-1, Errno=No space left on device (ENOSPC)
	[2018-12-08 21:33:54,013 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/themes/mkdocs/img WD=-1, Errno=No space left on device (ENOSPC)
	[2018-12-08 21:33:54,013 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/themes/mkdocs/__pycache__ WD=-1, Errno=No space left on device (ENOSPC)
	[2018-12-08 21:33:54,013 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/assets/search WD=-1, Errno=No space left on device (ENOSPC)
	[2018-12-08 21:33:54,014 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/assets/search/mkdocs WD=-1, Errno=No space left on device (ENOSPC)
	[2018-12-08 21:33:54,014 pyinotify ERROR] add_watch: cannot watch /usr/lib/python3/dist-packages/mkdocs/assets/search/mkdocs/js WD=-1, Errno=No space left on device (ENOSPC)
	[I 181208 21:33:54 server:283] Serving on http://127.0.0.1:1122
```
### Suggested solution

1. Open Terminal
2. Type this command
```sh
	echo fs.inotify.max_user_watches=65536 | sudo tee -a /etc/sysctl.conf
```
then
```sh
	sudo sysctl -p
```
##### If there are no problem, let's start writing! </br> 
```
الحمد لله
```