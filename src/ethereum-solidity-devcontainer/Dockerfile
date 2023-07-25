# syntax=docker/dockerfile:1.4


# Base Image
# =============================================================================
FROM ubuntu:22.04
# FROM ubuntu:20.04
# FROM ethereum/solc:0.8.20

RUN \
    apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y \
        software-properties-common \
        curl \
        wget \
        ca-certificates \
        libc6 \
        rsync 



RUN \
    # get install script and pass it to execute: 
    curl -sL https://deb.nodesource.com/setup_18.x | bash && \
    # and install node 
    apt-get install -y nodejs && \
    # confirm that it was successful 
    node -v && \
    # npm installs automatically 
    npm -v


# RUN snap install solc

RUN npm install -g solc


RUN \
    add-apt-repository -y ppa:ethereum/ethereum && \
    add-apt-repository -y ppa:ethereum/ethereum-dev && \
    apt-get update -y && \
    apt-get upgrade -y && \
    # apt-get install -y solc && \
    apt-get install -y ethereum


## Install the Hardhat (hh) shortcut tool
RUN npm install -g hardhat-shorthand

RUN npm install -g truffle ganache-cli


# WORKDIR /workspace


