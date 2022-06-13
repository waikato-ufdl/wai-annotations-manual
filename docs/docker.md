Rather than installing wai.annotations yourself in virtual environments, you can simply
make use of our pre-built [Docker images](https://hub.docker.com/repository/docker/waikatoufdl/wai.annotations) 
(for an introduction to Docker, please refer to [Docker for data scientists](https://www.data-mining.co.nz/docker-for-data-scientists/)). 

The following versions of *wai.annotations* are available as images:

* 0.7.5: `waikatoufdl/wai.annotations:0.7.5`
* 0.7.6: `waikatoufdl/wai.annotations:0.7.6`
* 0.7.7: `waikatoufdl/wai.annotations:0.7.7`
* latest: `waikatoufdl/wai.annotations:latest` (based on latest code in repositories)


# Example usage

The following command-line starts the 0.7.6 version of wai.annotations in interactive
mode, mapping the current directory (`pwd`) into the `/workspace` directory in the
container, to have access to the data in this directory:

```bash
docker run -u $(id -u):$(id -g) -v `pwd`:/workspace -it wai.annotations:0.7.6
```

# Graphical user interface

By default, Docker is aimed at worker processes or command-line execution. If you want 
to make use of graphical interfaces, like displaying images, then you need to do the following:

## Linux

```bash
xhost +local:root
```

Add the following arguments to your `docker run` command:

```bash
--env="DISPLAY" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw"
```

## Other platforms

Please refer to [this MOA blog post](https://moa.cms.waikato.ac.nz/how-to-use-moa-in-docker/)
on how to run graphical user interfaces from within Docker for other platforms.

# Redis

If you want to access a Redis instance outside of the container, then add the following to
your `docker run` command:

```bash
--net=host
```
