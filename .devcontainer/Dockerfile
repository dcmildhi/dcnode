# Use Ubuntu 24.04 as the base image
FROM ubuntu:24.04

# Install essential tools & performance tuning
RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y     curl git nano vim python3 python3-pip nodejs npm     build-essential cmake htop neofetch tlp     && apt clean && rm -rf /var/lib/apt/lists/*

# Enable ZRAM for better memory management
RUN apt install -y zram-tools &&     echo 'ALGO=lz4' > /etc/default/zramswap &&     echo 'PERCENT=50' >> /etc/default/zramswap &&     systemctl enable zramswap

# Set working directory
WORKDIR /workspaces/dcnode

# Default shell
CMD ["/bin/bash"]
