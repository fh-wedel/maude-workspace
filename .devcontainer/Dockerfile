FROM debian:trixie-slim

# Avoid prompts from apt.
ENV DEBIAN_FRONTEND=noninteractive

# This sets up a basic environment.

RUN apt-get update && apt-get install -y \
    git curl unzip \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# Install the Maude from curccent release 
WORKDIR /root/maude
RUN curl -L -o Maude-3.5.1-linux-x86_64.zip https://github.com/maude-lang/Maude/releases/download/Maude3.5.1/Maude-3.5.1-linux-x86_64.zip
RUN unzip Maude-3.5.1-linux-x86_64.zip && rm Maude-3.5.1-linux-x86_64.zip

# Set the default shell to bash instead of sh
ENV SHELL /bin/bash

