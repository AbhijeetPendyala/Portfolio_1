---
layout: post
title:  "Devops 102: setup a conda environment with tensorflow-gpu"
date:   2021-02-20
desc: "Tips"
keywords: "Devops, Commandline, SSH"
categories: [Devops]
tags: [Devops,SSH]
icon: icon-html
---

<ul>
    <li> create enviroment and activate it  </li>
</ul>

```
conda create --name env_name
conda activate env_name

```
<ul>
    <li> check the requirements.txt of the repo or PyPI package that needs to be installed.    </li>
    <li> Look for the requirements of python version, tensorflow (or tensorflow-gpu) version and 
         CUDA version if mentioned </li>
    <li> If only the tensorflow version is mentioned and nothing else; go to the tensorflow website and check 
         for versions of python, compiler, and cuda toolkit which go hand-in-hand</li>
    <li> Lets say; its requried to install tensorflow-gpu == 2.3.2 , which is compatible with 
         python 3.5-3.8, and cuda 10.1</li>
    <li> Note: Install seaborn first; it takes care of pandas and numpy</li>

</ul>


```
conda install python==3.8
conda install tensorflow-gpu
conda install jupyter
conda install Ipython
conda install -c conda-forge jupyter_contrib_nbextensions
conda install seaborn 
```

<ul>
    <li> Open juypter notebook and check if tensorflow-gpu import is working </li>
</ul>

```
import tensorflow as tf
!python3 -c 'import tensorflow as tf; print(tf.__version__)' 
from tensorflow.python.client import device_lib
print(device_lib.list_local_devices())
!pip show tensorflow
print("Num GPUs Available: ", len(tf.config.list_physical_devices('GPU')))

```

<ul>
    <li> Use multiple GPUs </li>
</ul>

```

physical_devices = tf.config.list_physical_devices('GPU') 
for gpu_instance in physical_devices: 
    tf.config.experimental.set_memory_growth(gpu_instance, True)

```

<ul>
    <li> Use multiple GPUs </li>
</ul>

```
strategy = tf.distribute.MirroredStrategy()
with strategy.scope():
       ***
       model.fit_generator()
       ***

```