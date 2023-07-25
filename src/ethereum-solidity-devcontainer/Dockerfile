# syntax=docker/dockerfile:1.4


# Base Image
# =============================================================================
# FROM ubuntu:latest


# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.202.5/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version (use hirsuite or bionic on local arm64/Apple Silicon): hirsute, focal, bionic
# ARG VARIANT="hirsute"
# ARG VARIANT="ubuntu-21.04"
# FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}
# FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-21.04



# Update all Ubuntu Packages
# RUN apt update && apt upgrade -y

# Install curl
# RUN apt install curl

# Install node.js
# RUN curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
# RUN apt install -y nodejs



RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y software-properties-common && \
    apt-get install -y curl && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update -y && \
    apt-get install -y ethereum solc && \
    curl -sL https://deb.nodesource.com/setup_14.x | bash && \
    apt-get install -y nodejs

## Install the Hardhat (hh) shortcut tool
RUN npm install -g hardhat-shorthand

RUN npm install -g truffle ganache-cli

# WORKDIR /workspace


