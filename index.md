---

layout: col-sidebar
altfooter: true
title: OWASP Nightingale
tags: Nightingale
level: 2
type: tool
pitch: Docker for Pentesters

---
<!--Logo and Social Links-->

![Nightingale Logo](assets\images\Nightingale.png)

[![OWASP Flagship](https://img.shields.io/badge/owasp-incubator-blue.svg)](https://www.owasp.org/index.php/Category:OWASP_Project#tab=Project_Inventory) 

![](https://img.shields.io/github/followers/RAJANAGORI?style=social) 
![](https://img.shields.io/github/stars/RAJANAGORI?style=social) 
[![](https://img.shields.io/badge/-Follow-black?style=social&logo=Linkedin)](https://www.linkedin.com/in/raja-nagori/) [![](https://img.shields.io/twitter/follow/RajaNagori7?style=social&label=Follow)](https://twitter.com/RajaNagori7)
![profile count](https://komarev.com/ghpvc/?username=www-project-nightingale&color=blue) 
[![Medium Badge](https://img.shields.io/badge/-@rajanagori-03a57a?style=flat-square&labelColor=000000&logo=Medium&link=https://medium.com/@rajanagori)](https://medium.com/@rajanagori)



<!--Description-->
## Description
In today's technological era, docker is the most powerful technology in each and every domain, whether it is Development, cyber security, DevOps, Automation, or Infrastructure.

Considering the demand of the industry, I would like to introduce my idea to create a NIGHTINGALE: docker image for pentesters.

This docker image is ready to use environment will the required tools that are needed at the time of pentesting on any of the scopes, whether it can be web application penetration testing, network penetration testing, mobile, API, OSINT, or Forensics.

The best part is you can either create an altered docker image or pull the pre-built docker image from the hub.

Some of the best features are listed below, I would highly recommend going through it and starting penetrating into the application.
Link to access tool list : [tool list](https://owasp.org/www-project-nightingale/)

### Pros
1.	No need to install multiple programming language support and multiple modules.
2.	Booting process is very fast as per the virtualization concept.
3.	Need as per use resource of the host machine.
4.	All pre-install tools are installed and if you install any new software or tool use can go with that option.
5.	You can perform vulnerability assessment and penetration testing of any scope.
6.	You can access this docker container via browser by calling your local address.

### Cons
1.  You can run the container over cloud server but can’t perform mobile pentesting.
2.  Creating tunnel with SSH can’t help you to provide the connection to your physical device or virtual environment.

Note: Nothing can be impossible, so I will definitely find a solution for the cons points 🤟

### Why? 
The Reason behind creating this Docker file is to make a platform-independent penetration toolkit. It includes all the useful tools that will be required for a penetration tester

## Device Requirements
- Operating System: Windows, Mac, Linux
- Docker engine installed as per the Operating System

## Tools Category
- Operating System tools (Windows, Mac, Linux)
- Compression tools (7zip, tar, zip)
- Development Essentials (Git, GitLab, etc)
- Programming Languages support (Python, Ruby, Java, etc)
- Exploit Frameworks (Metasploit, Exploit-DB, etc)
- Port Scanning tools (nmap,etc)
- Network tools (Tcpdump, etc)
- Forensic tools (exiftool,steghide, binwalk, foremost, etc)
- Red Team Tools (Metasploit, etc)
- Information Gathering tools 
## Tools List

### Operating System Tools
- Vim
- zsh
- locate
- tree
- htop
- snapd
### Compression Techniques Tools
- unzip 
- p7zip-full
### Development Essentials
- git 
- ruby  
- ruby-dev 
- bundler 
- bison 
- flex 
- autoconf 
- automake 
- ruby-full 
- make 
- curl 
- gnupg 
- patch 
- ruby-bundler 
- nasm 
- wget 
- smbclient
### Programming Language Support
- Python
- GO
- Nodejs
- Ruby
### Exploit Framework
- Metasploit

### Web VAPT Tools
- sqlmap
- HawkScan
- XSStrike
- Whatweb
- dirsearch
- Arjun
- Sublist3r
- massdns
- LinkedFinder
- masscan
- jwt_tool
- qreplace
- gf
- httprobe
- assetfinder
- waybackurls
### Port Scanning Tools
- Nmap
- Masscan
- Amass 
### Network Tool
- Traceroute
- telnt
- net-tools
- iputils-ping
- tcpdump
- openvpn
- whois
- host
- nmap
### Forensics Tools
- exiftool
- steghide
- binwalk
- foremost
### Red Team Tool
- Impact toolkit
### Information Gathering 
- Shodan
- Recon-ng
- Reconspider
- Xray
### Mobile Application Support (Android Only)
- mobsf
- adb
- apktool
- jadx
- RMS
### OS Selection
- Debian : Latest

## Under Development, stay tuned !! ;-)
- ~~Add more tools regarding web VAPT and Mobile VAPT~~
- ~~Add more tools related to team teaming~~
- ~~Shift the complete architecture to Multi-stage build concpet in docker to reduce the time of build and size of the image.~~

<!--Lisence-->
## Licensing
This program is free software. Everyone is permitted to copy and distribute verbatim copies
of this license document, but changing it is not allowed stated under GNU GENERAL PUBLIC LICENSE
