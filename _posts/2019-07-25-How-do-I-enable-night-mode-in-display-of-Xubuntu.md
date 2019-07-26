---
layout: post
title: How do I enable night mode in display of Xubuntu?
description: save your eyes
color: 391abc
author: masfitri
---

بسم الله الرحمن الرحيم
<br/><br/>
### Title
How do I enable night mode in display of Xubuntu?

### Level: 
`Beginner`<br/>

### Refrence:
- `https://askubuntu.com/questions/977221/how-do-i-enable-night-mode-in-display-of-xubuntu` <br/>
- `https://www.google.com`

### Purpose:
`So how can I enable night mode in my Xubuntu?`

### Suggested solution

The following instructions will not enable gnomes night mode. But will allow a nearly indistinguishable effect.

1. Install redshift<br/>
`sudo apt install redshift redshift-gtk` 

2. Edit GeoClue's config <br/>
`sudo nano /etc/geoclue/geoclue.conf`

3. Append the following lines to /etc/geoclue/geoclue.conf
{% highlight yml %}
[redshift]
allowed=true
system=false
users=
Configure redshift
{% endhighlight %}

Example of a manual config, for Copenhagen, Denmark. See Redshift homepage for an additional config example. Comment out or change the latitude and longitude for you location. <br/>
`nano ~/.config/redshift.conf`
{% highlight yml %}
[redshift]
temp-day=6500
temp-night=3700
location-provider=manual

[manual]
lat=55.7
lon=12.6
{% endhighlight %}