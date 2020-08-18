---
layout: post
title:  "Accessing GCP cloud console"
date:   2017-03-14
desc: "Go to commands"
keywords: "GCP, Commandline, SSH"
categories: [GCP]
tags: [GCP,SSH]
icon: icon-html
---
<ul>
    <li> Login to google cloud and start VM instance </li> 
    <li>Open google cloud sdk in PC or terminal on ubuntu </li> 
</ul>

```
gcloud init

```
<ul>
    <li> Select the project </li> 
    <li> Select the user  </li> 
</ul>

```
gcloud compute ssh jupyter@my-fastai-instance -- -L 8080:localhost:8080 

jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser 

```
<ul>
    <li> Open the link displayed on console along with token </li> 
    <li> Replace the IP address with external ephemeral IP or static IP of the cloud console </li> 
</ul>


---
