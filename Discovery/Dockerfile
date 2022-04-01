
#
# Docker image with the latest version of Ubuntu.
# With tools for discovery pre-installed.
#

# LATEST UBUNTU
FROM ubuntu:latest
ENV DEBIAN_FRONTEND=noninteractive

LABEL maintainer="D1al-T0ne"\
	email="d1al.t0ne@outlook.com"

# ENVIRONMENT VARIABLES
ENV TOOLS="/opt"

# INSTALL THE BASICS
RUN apt-get update \
	&& apt-get install -y --no-install-recommends --fix-missing \
	curl \
	chromium-browser \
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

# INSTALL GO
RUN wget https://golang.org/dl/go1.17.5.linux-amd64.tar.gz && \
	tar -C /usr/local -xzf go1.17.5.linux-amd64.tar.gz && \
	rm -rf go1.17.5.linux-amd64.tar.gz
ENV GOPATH "/root/go"
ENV PATH "$PATH:/usr/local/go/bin:$GOPATH/bin"

# SETUP AND INSTALL TOOLS
RUN mkdir tools
WORKDIR /tools/
RUN \
    # INSTALL ARJUN
    pip3 install arjun && \

    # INSTALL DIRSEARCH
    git clone https://github.com/maurosoria/dirsearch.git $TOOLS/dirsearch && \
    cd $TOOLS/dirsearch && \
    pip3 install -r requirements.txt && \

    # INSTALL GAU
    wget https://github.com/lc/gau/releases/download/v1.1.0/gau_1.1.0_linux_amd64.tar.gz && \
    tar xvf gau_1.1.0_linux_amd64.tar.gz &&\
    rm -rf tar xvf gau_1.1.0_linux_amd64.tar.gz && \
    mv gau /usr/bin/gau && \

	# INSTALL KITERUNNER
    wget https://github.com/assetnote/kiterunner/releases/download/v1.0.1/kiterunner_1.0.1_linux_amd64.tar.gz &&\
	tar xvf kiterunner_1.0.1_linux_amd64.tar.gz && \
	rm -rf tar xvf kiterunner_1.0.1_linux_amd64.tar.gz && \
	mv kr /usr/bin/kr && \

    # INSTALL LINKFINDER
    git clone https://github.com/GerbenJavado/LinkFinder.git $TOOLS/linkfinder && \
    cd $TOOLS/linkfinder && \
    python3 setup.py install && \
    pip3 install -r requirements.txt && \

    # INSTALL PARAMSPIDER
    git clone https://github.com/devanshbatham/ParamSpider $TOOLS/ParamSpider && \
    cd $TOOLS/ParamSpider && \
    pip3 install -r requirements.txt && \

	## INSTALL SUBJS
	go get -u -v github.com/lc/subjs@latest && \

	# INSTALL UNFURL
	go get -u github.com/tomnomnom/unfurl

# ADD THE INSTALL SCRIPT AND RUN
ADD install.sh /
RUN chmod +x /install.sh
RUN /install.sh
