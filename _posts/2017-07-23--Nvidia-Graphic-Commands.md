---
layout: post
title:  "Nvidia Graphic commands"
date:   23-07-2017
desc: "Go to commands"
keywords: "GCP, Commandline, SSH"
categories: [Nvidia]
tags: [Nvidia,SSH]
icon: icon-html
---
<ul>
    <li> Monitor GPU usage (live) </li> 
</ul>

```
watch -n0.5 nvidia-smi

```
<ul>
    <li> To check CUDA is installed </li> 
</ul>

```
nvidia-smi

```
<ul>
    <li> Open the link displayed on console along with token </li> 
    <li> Replace the IP address with external ephemeral IP or static IP of the cloud console </li> 
</ul>


---
<ul>
    <li> list the gpus </li>
</ul>

```

nvidia-smi --list-gpus

```
