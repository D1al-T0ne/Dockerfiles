## Discovery
An Ubuntu Docker instance with the latest version, utility tools pre-installed along with a collection of community tools used in the discovery processes.

## Usage
1. You need [Docker](https://docs.docker.com/get-docker/) installed.<br>
2. Copy the Dockerfile and install.sh script to a directory of your choice.
3. Build the docker container.<br>
```bash
docker buid -t discovery .
```
4. After building the image, you can run it directly from the command-line:
```bash
docker run -v `pwd':/srv/ -it --rm discovery
```
Or save a function to quickly spin this instance up, with persistant storage:<br>
```bash
function discovery(){
  dirname=${PWD##*/}
  docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm discovery
}
```

## Tools

| Tool | Repository |
|---|---|
|arjun|https://github.com/s0md3v/Arjun|
|dirsearch|https://github.com/maurosoria/dirsearch|
|gau|https://github.com/lc/gau|
|kiterunner|https://github.com/assetnote/kiterunner|
|linkfinder|https://github.com/GerbenJavado/LinkFinder|
|subjs|https://github.com/lc/subjs|
|unfurl|https://github.com/tomnomnom/unfurl|

## Feedback
If you have any tips or improvement ideas I should be working on please let me [know.](https://github.com/D1al-T0ne/Dockerfiles/Discovery/Issues)

[![D1al T0ne](https://aleen42.github.io/badges/src/twitter.svg)](https://twitter.com/D1AL__T0NE)<br>
