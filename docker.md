# docker

## nsenter to overlay namespace

nsenter --net=/var/run/docker/netns/1-<overlay id>

## nsenter to docker namespave 

nsenter --net=$(docker inspect <container_name> | jq .[].NetworkSettings.SandboxKey)

