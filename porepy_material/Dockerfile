# PorePy workshop image for JupyterHub/Jupyter Docker Stacks
#
# Build example:
#   docker build -t ghcr.io/<your-user>/porepy-workshop:latest porepy_material
#
# The image extends a Jupyter Docker Stacks base image so it works well with
# JupyterHub deployments that already use those images.

FROM quay.io/jupyter/scipy-notebook:2025-12-31

USER root

# System libraries needed by gmsh / plotting / scientific stack.
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    git \
    libglu1-mesa \
    libgl1 \
    libxrender1 \
    libxcursor1 \
    libxft2 \
    libxinerama1 \
    libsm6 \
    libxext6 \
    ffmpeg \
    python3-tk \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}
WORKDIR /home/jovyan

# Install PorePy from source and fetch the workshop material.
RUN git clone --depth 1 --branch develop https://github.com/pmgbergen/porepy.git /home/jovyan/porepy \
    && python -m pip install --no-cache-dir --upgrade pip \
    && python -m pip install --no-cache-dir -e '/home/jovyan/porepy[testing]' \
    && python -m pip install --no-cache-dir pypardiso \
    && git clone --depth 1 https://github.com/keileg/dfn_workshop_porepy.git /home/jovyan/porepy_material

WORKDIR /home/jovyan/porepy_material

# Default to JupyterLab via the docker-stacks startup command.
CMD ["start-notebook.py", "--ServerApp.root_dir=/home/jovyan/porepy_material"]
