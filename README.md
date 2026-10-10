# alpine-minidlna
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721/alpine-minidlna)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721/alpine-minidlna)



----------------------------------------
### amd64
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721/alpine-minidlna/latest?arch=amd64)
### arm64
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721/alpine-minidlna/latest?arch=arm64)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : amd64, arm64
* Application : [ReadyMedia](https://sourceforge.net/projects/minidlna/)
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
           forumi0721/alpine-minidlna:latest
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

