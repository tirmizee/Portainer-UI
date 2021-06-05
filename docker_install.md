
##### run in docker

    docker run -d --name portainer -p 9000:9000 -v "/var/run/docker.sock:/var/run/docker.sock"  portainer/portainer

##### run in swarm

    docker service create -d --name portainer -p 9000:9000 --mount type=volume,source=/var/run/docker.sock,destination=/var/run/docker.sock portainer/portainer
