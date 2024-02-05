# Start from a base Debian or Ubuntu image since they typically have easy access to Gforth via package managers.
FROM debian:bullseye-slim

# Avoid prompts from apt.
ENV DEBIAN_FRONTEND=noninteractive

# This sets up a basic environment
RUN apt-get update && apt-get install -y \
    git make docker.io \
    # You can include other necessary tools here, depending on your development needs.
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

RUN ln -s /workspaces /root/Projects

# Set the default shell to bash instead of sh
ENV SHELL /bin/bash
