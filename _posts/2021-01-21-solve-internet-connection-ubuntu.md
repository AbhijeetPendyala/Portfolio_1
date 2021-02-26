---
layout: post
title:  "Solve internet connection issues without restarting ubuntu"
date:   2021-01-21
desc: "Tips"
keywords: "Ubuntu, Commandline"
categories: [Internet]
tags: [Internet,SSH]
icon: icon-html
---

<ul>
    <li> Usually, its due to DNS cache </li>
</ul>

```
sudo /etc/init.d/dns.clean start

```
<ul>
    <li> If not; restart the network manager </li>

</ul>


```
sudo /etc/init.d/networking restart
sudo /etc/init.d/networking status
```
