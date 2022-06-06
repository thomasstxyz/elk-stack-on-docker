# Introduction

This docker composition installs the ELK stack on a local Docker node.

# Setup

Clone the repository and change into the directory.

    git clone https://github.com/thomasstxyz/elk-stack-on-docker
    cd elk-stack-on-docker

Increase sysctl parameter for Elasticsearch.

    sudo sysctl -w vm.max_map_count=262144
    echo "vm.max_map_count=262144" | sudo tee --append /etc/sysctl.conf

Modify the variables in `.env`.

    nano .env

Run docker compose:

    docker compose up -d

Now visit the Kibana dashboard in a Browser at `http://<node_ip>:5601`.
