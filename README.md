<h3 align="center">Dockerfiles</h3>


The goal is to have have a collection of specific purpose containers.

## Images
A base Ubuntu Docker instance can quickly be spun up from the command line:
```bash 
docker run -it --rm --entrypoint "/bin/bash" ubuntu:latest
```
(Note: no persistent storage)

<h3>Ubuntu</h3>
An Ubuntu Docker instance with the latest version and utility tools pre-installed.<br>
Use a function to quickly spin this instance up, with persistant storage.

```bash
function ubuntu () {
	dirname=${PWD##*/}
	docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm ubuntu
}
```
<h3>Discovery</h3>
An Ubuntu Docker instance with the latest version, utility tools pre-installed and<br>
a collection of tools used in the discovery processes.

```bash
function discovery(){
  dirname=${PWD##*/}
  docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm discovery
}
```
## Environment
The Base Teriminal and Ubuntu images here have been tested:
- Docker Desktop on Mac (Intel): Version 3.6.0, Engine 20.10.8

## Credits
This repository was inspired by the blog post [Docker for Pentesters](https://blog.ropnop.com/docker-for-pentesters/)<br>
