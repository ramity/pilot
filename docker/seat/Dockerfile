FROM ubuntu:24.04

# Update apt
RUN apt update
RUN apt upgrade -y

# Install gemini-cli
RUN apt install -y nodejs
RUN apt install -y npm
RUN npm install -g @google/gemini-cli

# Install neovim
RUN apt install -y neovim

# Keep container open
ENTRYPOINT sleep infinity
