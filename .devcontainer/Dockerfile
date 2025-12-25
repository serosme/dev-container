FROM node:24-trixie

# RUN sed -i 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
#     locale-gen

# ENV LANG=en_US.UTF-8

COPY debian.sources /etc/apt/sources.list.d/debian.sources

RUN apt update && \
    apt upgrade -y && \
    apt install -y sudo && \
    echo "node ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN corepack enable pnpm

ENTRYPOINT ["sleep", "infinity"]
