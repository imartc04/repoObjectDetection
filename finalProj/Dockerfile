# Use the nvidia/cuda12.0.1-devel base image
FROM nvidia/cuda:11.8.0-cudnn8-devel-ubuntu22.04

# Install additional packages
RUN apt update && apt install -y curl nano iputils-ping bash-completion

# Set an alias for "ls -l" to "ll"
RUN echo "alias ll='ls -l'" >> ~/.bashrc


# Install Python 3 and Conda
RUN apt update && apt install -y python3 python3-pip
RUN curl -sSL https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o /tmp/miniconda.sh \
    && bash /tmp/miniconda.sh -bfp /usr/local \
    && rm -rf /tmp/miniconda.sh \
    && conda clean -afy


# Set the default command to run when the container starts
CMD ["/bin/bash"]
