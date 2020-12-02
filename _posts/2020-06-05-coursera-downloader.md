---
layout: post
title:  "Downloading the course content from registered courses on coursera"
date:   2020-06-06
desc: "Go to commands"
keywords: "GCP, Commandline, SSH"
categories: [Terminal]
tags: [Terminal,Git, Coursera]
icon: icon-html
---
<ul>
    <li> Login to coursera account </li> 
    <li> Login into ai37 or other conda environment where coursera dl installed </li> 
    <li> copy the cauth value of the course from browser. Right click in chrome 
         on the course page after login-> go to inspect->application->cookies->cauth </li> 
    <li> coursera-dl -ca (cauth value) (course-name) </li> 
</ul>
