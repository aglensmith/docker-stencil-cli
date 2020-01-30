# docker-stencil-cli
Docker file for BigCommerce's Stencil CLI

## Usage

Build and run:

```bash
# build docker image
docker build -t docker-stencil github.com/aglensmith/docker-stencil.git

# move into theme dir
cd ~/theme/dir

# run image with interactive shell
sudo docker run -it -v $(pwd):/theme -p3000:3000 docker-stencil /bin/bash
```

| Option           | Description                                                    |                                                                
|------------------|----------------------------------------------------------------|
|`-it`             |Keep STDIN open even if not attached, allocate a pseudo-TTY     |
|`-v $(pwd):/theme`|Mount host's current working directory to container WORKDIR     |
|`-p3000:3000`     |Expose stencil's default port to localhost                      |
|`/bin/bash`       |Specify bash as the shell to use so we can run stencil commands |


In the container's bash shell, run:

``bash
stencil init

stencil start
```
