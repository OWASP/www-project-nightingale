---
title: Installation Guide
layout:  null
altfooter: true
tab: true
order: 2
tags: Nightingale
---
## Docker Image Build and Run 
- Take a clone of the repository
```
git clone --depth 1 https://github.com/RAJANAGORI/Nightingale.git
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
- Now, you can directly access Nightingale interactive terminal using the browser
```
docker run -it -p 0.0.0.0:8080:7681 -d rajanagori/nightingale /home/binaries/ttyd -p 7681 bash
```
### If you want to run MobSF along with the nightingale then I will give you good news now you can do the same....!!
#### part 1
```
docker run -it -p 0.0.0.0:8080:7681 -p 0.0.0.0:8081:8081 -d rajanagori/nightingale /home/binaries/ttyd -p 7681 bash 
```
#### part 2
```
cd /home/tools_mobile_vapt/Mobile-Security-Framework-MobSF/
source venv/bin/activate
./run 0.0.0.0:8081 &
```
- Call your browser and hit 127.0.0.1:8080 for the nightingale terminal and 127.0.0.1:8081 for MobFs to become you will be prooo!!!!

- If you want to bind your host machine directory to your container directory then you can do the same.
```
docker run -it -p 0.0.0.0:8080:7681 -p 0.0.0.0:8081:8081 -v /<your_host_machine_directory_path>:/<your_container_directory_path> -d rajanagori/nightingale /home/binaries/ttyd -p 7681 bash
```

### For Localtunnel
- Hit 127.0.0.1:8080 in your browser and you will be able to access the Nightingale terminal
- Now, run the following command in your terminal
```
lt --port 7681 --subdomain nightingale
```
### To start Runtime Mobile Security Framework
#### part 1
```
docker run -it -p 0.0.0.0:8080:7681 -p 0.0.0.0:8081:8081 -p 0.0.0.0:5000:5000 -d rajanagori/nightingale /home/binaries/ttyd -p 7681 bash
```
#### part 2
```
cd tools_mobile_vapt/rms && pm2 start rms.js --name rms
```
Now, hit 127.0.0.1:8080 and have fun with Nightingale !!!
## To start, Restart and Stop the Postgresql database 
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