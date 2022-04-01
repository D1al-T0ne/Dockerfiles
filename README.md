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

<h3>Discovery</h3>
An Ubuntu Docker instance with the latest version, utility tools pre-installed along with
a collection of community tools used in the discovery processes.

## Environment
The Base Teriminal, Ubuntu, and Dicovery images here have been tested on:
- Docker Desktop on Mac (Intel): Version 3.6.0, Engine 20.10.8

## Credits
This repository was inspired by the blog post [Docker for Pentesters](https://blog.ropnop.com/docker-for-pentesters/)<br>

## Feedback
If you have any tips or improvement ideas I should be working on please let me [know.](https://github.com/D1al-T0ne/Dockerfiles/Issues)

[![D1al T0ne](https://aleen42.github.io/badges/src/twitter.svg)](https://twitter.com/D1AL__T0NE)<br>
