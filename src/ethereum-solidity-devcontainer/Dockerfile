# syntax=docker/dockerfile:1.4


# Base Image
# =============================================================================
# FROM ubuntu:22.04
FROM ubuntu:18.04


RUN \
    apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y \
        software-properties-common \
        curl \
        wget \
        ca-certificates \
        rsync 

RUN \
    add-apt-repository -y ppa:ethereum/ethereum && \
    add-apt-repository -y ppa:ethereum/ethereum-dev && \
    apt-get update -y && \
    apt-get upgrade -y

RUN \
    apt-get install -y solc && \
    apt-get install -y ethereum
        


RUN \
    # get install script and pass it to execute: 
    curl -sL https://deb.nodesource.com/setup_18.x | bash && \
    # and install node 
    apt-get install -y nodejs && \
    # confirm that it was successful 
    node -v && \
    # npm installs automatically 
    npm -v

## Install the Hardhat (hh) shortcut tool
RUN npm install -g hardhat-shorthand

RUN npm install -g truffle ganache-cli

# WORKDIR /workspace


