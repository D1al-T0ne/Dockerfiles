## Ubuntu
An Ubuntu Docker instance with the latest version and utility tools pre-installed.<br>

## Usage
1. You need [Docker](https://docs.docker.com/get-docker/) installed.<br>
2. Copy the Dockerfile and install.sh script to a directory of your choice.
3. Build the docker container.<br>
```bash
docker buid -t ubuntu .
```
4. After building the image, you can run it directly from the command-line:
```bash
docker run -v `pwd':/srv/ -it --rm ubuntu
```
Or save a function to quickly spin this instance up, with persistant storage:<br>
```bash
function ubuntu () {
	dirname=${PWD##*/}
	docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm ubuntu
	}
```

## Feedback
If you have any tips or improvement ideas I should be working on please let me [know.](https://github.com/D1al-T0ne/Dockerfiles/Ubuntu/Issues)

[![D1al T0ne](https://aleen42.github.io/badges/src/twitter.svg)](https://twitter.com/D1AL__T0NE)<br>
