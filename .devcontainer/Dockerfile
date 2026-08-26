# .devcontainer/Dockerfile

# Base Image
FROM ubuntu:24.04

# Interactive Mode
ENV DEBIAN_FRONTEND=noninteractive

# Install Dependencies
RUN apt-get update -y 
RUN apt-get install -y --no-install-recommends curl git 
RUN apt-get install -y --no-install-recommends build-essential python3 python3-pip

# Install Node Version 24
RUN curl -fsSL https://deb.nodesource.com/setup_24.x | bash
RUN apt-get install -y --no-install-recommends nodejs

RUN npm install -g pnpm

# Clean Up
RUN apt-get clean -y
RUN rm -rf /var/lib/apt/lists/*