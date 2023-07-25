# syntax=docker/dockerfile:1.4


# Base Image
# =============================================================================
FROM ubuntu:latest

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update -y && \
    apt-get install -y ethereum solc && \
    curl -sL https://deb.nodesource.com/setup_14.x | bash && \
    apt-get install -y nodejs

RUN npm install -g truffle ganache-cli

WORKDIR /workspace
