FROM ubuntu:24.04

# Update apt
RUN apt update
RUN apt upgrade -y

# Nvm deps
RUN apt install -y git
RUN apt install -y curl
RUN apt install -y libatomic1

# Install nvm using defined install script
COPY docker/seat/install-nvm.sh install-nvm.sh
RUN ./install-nvm.sh
RUN bash -c "source /root/.nvm/nvm.sh && nvm install 25.2.0"
RUN bash -c "source /root/.nvm/nvm.sh && nvm use 25.2.0"

# Install gemini-cli
RUN bash -c "source /root/.nvm/nvm.sh && npm install -g @google/gemini-cli"

# Install neovim
RUN apt install -y neovim

# Keep container open
ENTRYPOINT sleep infinity
