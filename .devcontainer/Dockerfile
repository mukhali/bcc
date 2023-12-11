# FROM mcr.microsoft.com/devcontainers/python:3
# FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04
FROM mcr.microsoft.com/devcontainers/base:debian-12
# FROM linuxkit/kernel:4.14.12 AS kernel

# Copy environment.yml (if found) to a temp location so we update the environment. Also
# copy "noop.txt" so the COPY instruction does not fail if no environment.yml exists.
# COPY environment.yml* .devcontainer/noop.txt /tmp/conda-tmp/
# RUN if [ -f "/tmp/conda-tmp/environment.yml" ]; then umask 0002 && /opt/conda/bin/conda env update -n base -f /tmp/conda-tmp/environment.yml; fi \
#     && rm -rf /tmp/conda-tmp

# [Optional] Uncomment to install a different version of Python than the default
# RUN conda install -y python=3.6 \
#     && pip install --no-cache-dir pipx \
#     && pipx reinstall-all

# RUN echo deb http://cloudfront.debian.net/debian sid main >> /etc/apt/sources.list \
#     && apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends bpfcc-tools libbpfcc libbpfcc-dev linux-headers-$(uname -r)

RUN <<EOT
  echo deb http://mirrors.ustc.edu.cn/debian/ bookworm contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo # deb-src http://mirrors.ustc.edu.cn/debian/ bookworm contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo deb http://mirrors.ustc.edu.cn/debian/ bookworm-updates contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo # deb-src http://mirrors.ustc.edu.cn/debian/ bookworm-updates contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo deb http://mirrors.ustc.edu.cn/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo # deb-src http://mirrors.ustc.edu.cn/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo deb http://mirrors.ustc.edu.cn/debian/ bookworm-backports contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo # deb-src http://mirrors.ustc.edu.cn/debian/ bookworm-backports contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo deb http://mirrors.ustc.edu.cn/debian-security/ bookworm-security contrib main non-free non-free-firmware >> /etc/apt/sources.list
  echo # deb-src http://mirrors.ustc.edu.cn/debian-security/ bookworm-security contrib main non-free non-free-firmware >> /etc/apt/sources.list
  apt-get update
EOT

# RUN <<EOT
#   echo deb https://mirrors.ustc.edu.cn/ubuntu/ jammy main restricted universe multiverse >> /etc/apt/sources.list
#   echo # deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy main restricted universe multiverse >> /etc/apt/sources.list
#   echo deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-security main restricted universe multiverse >> /etc/apt/sources.list
#   echo # deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-security main restricted universe multiverse >> /etc/apt/sources.list
#   echo deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse >> /etc/apt/sources.list
#   echo # deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse >> /etc/apt/sources.list
#   echo deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse >> /etc/apt/sources.list
#   echo # deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse >> /etc/apt/sources.list
#   echo # 预发布软件源，不建议启用 >> /etc/apt/sources.list
#   echo # deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse >> /etc/apt/sources.list
#   echo # deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse >> /etc/apt/sources.list
#   apt-get update
# EOT
