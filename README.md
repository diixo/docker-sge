docker-sge
==========

Dockerfile to build a container with SGE installed.

To build type:

```
git clone git@github.com:gawbul/docker-sge.git
cd docker-sge
docker build -t gawbul/docker-sge .
```

To pull from the Docker Hub type:

```
docker pull gawbul/docker-sge
```

To run the image in a container type:

```
docker run -it --rm gawbul/docker-sge login -f sgeadmin
```

**You need the `login -f sgeadmin` as root isn't allowed to submit jobs**

To submit a job run:

```
echo "echo Running test from $HOSTNAME" | qsub
```


## References:

https://hub.docker.com/r/robsyme/docker-sge

https://github.com/epam/grid-engine-api/blob/develop/docker/sge/Dockerfile

https://github.com/jedisct1/phusion-baseimage-latest/blob/master/Changelog.md

https://github.com/gridengine/config-api/blob/master/etc/uge.conf
