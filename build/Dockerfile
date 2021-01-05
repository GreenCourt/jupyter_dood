FROM python:3.8
RUN apt-get update && apt-get install -y gosu && apt-get clean && rm -rf /var/lib/apt/lists/*
ARG DOCKER_CLIENT_VERSION
RUN curl -L  https://download.docker.com/linux/static/stable/x86_64/docker-${DOCKER_CLIENT_VERSION}.tgz \
    | tar -xzC /usr/local/bin --strip=1 docker/docker 
RUN pip install --no-cache-dir jupyterlab jupyterlab-classic
