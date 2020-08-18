---
layout: post
title:  "Docker Tips"
date:   2019-08-13
desc: "Go to commands"
keywords: "GCP, Commandline, SSH"
categories: [Docker Containers]
tags: [Docker,SSH]
icon: icon-html
---

<ul>
    <li> list active docker images </li>  
</ul>

```
docker ps -all

```
<ul>
    <li> copy files into container  </li>  
</ul>

```
docker cp upload.zip infallible_chebyshev:/workspace upload.zip 

docker cp upload.zip b58e39a29aa7:/workspace upload.zip 

```
<ul>
    <li> copy files from container to host  </li>  
</ul>

```

sudo docker cp 936ecaf3748b:/workspace/TensorRT-Yolov3/yolov3_fp16..engine ~ 


```

<ul>
    <li> start new container from an Image </li>  
</ul>

```

docker run IMAGE

```

<ul>
    <li> Adds the files in the local repository and stages them for commit, 
        To stage specific file, use its filename </li>  
</ul>

```
git add .

```

<ul>
    <li>  Remove a container </li>  
</ul>

```

docker rm CONTAINER

```

<ul>
    <li> start/stop a container  </li>  
</ul>

```

docker start/stop CONTAINER

```

<ul>
    <li> open a terminal inside container </li>  
</ul>

```
docker exec -it CONTAINER EXECUTABLE

```

<ul>
    <li> Create an image from container </li>  
</ul>

```
docker commit CONTAINER 

```


<ul>
    <li> Remove and image </li>  
</ul>

```
docker rmi IMAGE

```

<ul>
    <li> Build image from docker file </li>  
</ul>

```
docker build DIRECTORY

```

<ul>
    <li> Download or upload image </li>  
</ul>

```
docker pull/push IMAGE


```



















---

