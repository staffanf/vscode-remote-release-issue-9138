FROM ubuntu:jammy

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get --no-install-recommends install -y \
  git \
  iproute2 \
  iputils-ping \
  nano \
  pkg-config \
  python3 \
  python3-pip \
  python3-venv \
  python-is-python3 \
  software-properties-common \
  wget \
  bash-completion \
  && rm -rf /var/lib/apt/lists/*

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
RUN groupadd --gid $USER_GID $USERNAME \
  && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

USER $USERNAME
