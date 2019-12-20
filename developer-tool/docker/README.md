# Docker

### Docker install on Ubuntu
```sh

$ sudo apt-get update
$ sudo apt-get install /
    apt-transport-https /
    ca-certificates /
    curl /
    gnupg-agent /
    software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository /
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu /
   $(lsb_release -cs) /
   stable"
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### check version engine
```sh
$ docker version
```
---
### Docker Images 
#### ดู docker images
```sh
$ docker images
```
#### ลบ docker images 
```sh
$ docker rmi <images_name || id>
```

#### ลบ docker images ที่ไม่ใช้ทั้งหมด
```sh
$ docker image prune -a
```
---
### Docker Container
#### ดู container ที่ รันอยู่
```sh 
$ docker container ls
หรือ 
$ docker ps
```

#### ดู logs ของ container นั้นๆ
```sh
$ docker container logs <container_name>
หรือ 
$ docker logs <container_name>
```

#### Remove Container
```sh
$ docker rm <container_name || id>
```
#### ลบ Container ทั้งหมดที่ไม่ถูกใช้
```sh
$ docker container prune
```
