FROM carlodepieri/docker-archlinux-systemd
LABEL maintainer="depieri.carlo@gmail.com"

# Use bash while building the image
SHELL ["/bin/bash", "-c"]

# Install python & pip
RUN pacman -Syu python python-pip git --noconfirm && \
yes | pacman -Scc

# Upgrade pip to latest version.
RUN pip install --upgrade pip

# Prepare the cgroup volume
VOLUME [ "/sys/fs/cgroup" ]

# Start systemd at init
CMD ["/lib/systemd/systemd"]
