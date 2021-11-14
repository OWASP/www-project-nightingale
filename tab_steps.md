---
title: Overview
layout:  null
altfooter: true
tab: true
order: 1
tags: Nightingale
---

## Docker for Pentesters
### Project Name: Nightingale
==================================================
### Docker for Pentesters: Pentesting Framework 

### Docker Image build and Run 
- Take a clone of the repository
```
git clone https://github.com/RAJANAGORI/Nightingale.git
```
- Change the Directory
```
cd Nightingale
```
- Now build the Docker Image.
```
docker build -t rajanagori/nightingale .
```
- After Creating the Docker Image, Login into the image and Happy Hacking.... ;-)
```
 docker run -ti --hostname nightingale  rajanagori/nightingale /bin/bash
```

### To start, Restart and Stop the Postgresql database 
- To start the service
```
service postgresql start
```
- To Restart the service
```
service postgresql restart
```
- To Stop the service
```
service postgresql stop
```

Note: Use of Postgresql is for msfConsole.
