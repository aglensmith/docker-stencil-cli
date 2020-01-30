# docker-stencil-cli
Dockerfile for BigCommerce's Stencil CLI

## Installation

```bash
# build docker image
docker build -t docker-stencil https://github.com/aglensmith/docker-stencil-cli.git
```

## Usage

```bash
cd ~/theme/dir

sudo docker run -it -v $(pwd):/theme -p3000:3000 docker-stencil stencil start
```

| Option           | Description                                                    |                                                                
|------------------|----------------------------------------------------------------|
|`-it`             |Keep STDIN open even if not attached, allocate a pseudo-TTY     |
|`-v $(pwd):/theme`|Mount host's current working directory to container WORKDIR     |
|`-p3000:3000`     |Expose stencil's default port to localhost                      |

Or start in a bash shell:

```bash
sudo docker run -it -v $(pwd):/theme -p3000:3000 docker-stencil /bin/bash
```
