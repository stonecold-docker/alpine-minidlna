# alpine-minidlna
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721/alpine-minidlna)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721/alpine-minidlna)



----------------------------------------
### x64
![Docker Image Version](https://img.shields.io/docker/v/forumi0721/alpine-minidlna/latest)
![Docker Image Size](https://img.shields.io/docker/image-size/forumi0721/alpine-minidlna/latest)
### aarch64
![Docker Image Version](https://img.shields.io/docker/v/forumi0721/alpine-minidlna/aarch64)
![Docker Image Size](https://img.shields.io/docker/image-size/forumi0721/alpine-minidlna/aarch64)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : x64,aarch64
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
           forumi0721/alpine-minidlna:[ARCH_TAG]
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

