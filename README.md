# alpine-minidlna

#### [alpine-x64-minidlna](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-minidlna/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpinex64/alpine-x64-minidlna/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpinex64/alpine-x64-minidlna/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpinex64/alpine-x64-minidlna/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinex64/alpine-x64-minidlna)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinex64/alpine-x64-minidlna)
#### [alpine-aarch64-minidlna](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-minidlna/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpineaarch64/alpine-aarch64-minidlna/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpineaarch64/alpine-aarch64-minidlna/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpineaarch64/alpine-aarch64-minidlna/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpineaarch64/alpine-aarch64-minidlna)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpineaarch64/alpine-aarch64-minidlna)
#### [alpine-armhf-minidlna](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-minidlna/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpinearmhf/alpine-armhf-minidlna/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpinearmhf/alpine-armhf-minidlna/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpinearmhf/alpine-armhf-minidlna/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinearmhf/alpine-armhf-minidlna)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinearmhf/alpine-armhf-minidlna)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : x64,aarch64,armhf
* Appplication : [ReadyMedia](https://sourceforge.net/projects/minidlna/)
    - ReadyMedia (formerly known as MiniDLNA) is a simple media server software, with the aim of being fully compliant with DLNA/UPnP-AV clients.



----------------------------------------
#### Run

```sh
docker run -d \
           --net=host \
           -p 8200:8200/tcp \
           -v /data:/data \
           -e FRIENDLY_NAME="DLNA Server" \
           -e MEDIA_DIR=/data \
           forumi0721alpine[ARCH]/alpine-[ARCH]-minidlna:latest
```



----------------------------------------
#### Usage

* Nothing to do. Just set the client.



----------------------------------------
#### Docker Options

| Option             | Description                                      |
|--------------------|--------------------------------------------------|
| --net=host         | Host mode                                        |


#### Ports

| Port               | Description                                      |
|--------------------|--------------------------------------------------|
| 8200/tcp           | Listen port for minidlna daemon                  |


#### Volumes

| Volume             | Description                                      |
|--------------------|--------------------------------------------------|
| /data              | Media directory                                  |


#### Environment Variables

| ENV                | Description                                      |
|--------------------|--------------------------------------------------|
| FRIENDLY_NAME      | the name that shows up on your clients. (default : DLNA Server) |
| MEDIA_DIR          | Directory you want scanned. (default : /data)    |
| NETWORK_INTERFACE  | Network interface for broadcast                  |

