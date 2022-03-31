
#
# Docker image with the latest version of Ubuntu.
# With some basics installed.
#

FROM ubuntu:latest
ENV DEBIAN_FRONTEND=noninteractive

LABEL maintainer="D1al-T0ne"\
	email="d1al.t0ne@outlook.com"

# INSTALL THE BASICS
RUN apt-get update \
	&& apt-get install -y --no-install-recommends --fix-missing \
	curl \
	chromium-browser \
	default-jdk \
	dnsutils \
	findutils \
	git \
	jq \
	npm \
	python3 \
	python3-pip \
	screen \
	vim \
	vim-gtk3 \
	wget \
	whois

# ADD THE INSTALL SCRIPT AND RUN
ADD install.sh /
RUN chmod +x /install.sh
RUN /install.sh
