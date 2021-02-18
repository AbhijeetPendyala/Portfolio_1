---
layout: post
title:  "Devops 101: Install dependencies in a python venv"
date:   2017-03-17
desc: "Tips"
keywords: "Devops, Commandline, SSH"
categories: [Devops]
tags: [Devops,SSH]
icon: icon-html
---
<ul>
    <li> setup tensorflow and jupyter notebook in ./venv </li>
    <li> Open a new jupyter notebook from ./venv </li>

</ul>


```
sudo apt install python3-dev python3-pip python3-venv
python3 -m venv --system-site-packages ./venv
source ./venv/bin/activate
pip install --upgrade pip
pip list 
pip install --upgrade tensorflow
pip install --upgrade tensorflow-gpu
ipython kernel install --user --name=.venv
jupyter notebook
```

<ul>
    <li> sys path commands </li>
</ul>

```
import sys
sys.executable
sys.path.remove('/path/you/dont/want')
sys.path.append('/path/you/do/want')

```