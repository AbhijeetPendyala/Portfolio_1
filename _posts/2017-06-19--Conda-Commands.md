---
layout: post
title:  "Quick Conda commands"
date:   2017-06-19
desc: "Tips"
keywords: "Conda, Devops, Commandline"
categories: [Devops]
tags: [Devops,SSH]
icon: icon-html
---

<ul>
    <li> create enviroment and activate it  </li>
</ul>

```
conda create --name env_name python=3.7
conda activate env_name

```

<ul>
    <li> export the packages used in the current environment to an environment file  </li>
</ul>

```
conda env export > environment.yaml

```

<ul>
    <li> create enviroment from existing yaml file </li>
</ul>

```
conda env create --file environment.yaml

```
