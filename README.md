# zeta-Docker

This project helps you to setup zeta.

## Setup

First check this repository out. After that checkout the zeta/modigen repository. And copy it as modigen-v3 into zeta-docker or you could just adjust the docker-compose.yml and write in your own paths.

```
git clone https://github.com/HTWG-VirtualReality/zeta-docker.git
cd zeta-docker
git clone https://bitbucket.org/mgerhart/modigen-v3.git
cd modigen-v3
git fetch && git checkout vr-editor
cd ../
```

Besides these step you should also have ```docker``` and ```docker-compose``` installed.

## Usage

Just execute ```docker-compose up``` within zeta-docker folder and the containers gets started. Only at the first execution it will take very long (ca. 20-30 min) for retrieving all dependencies.
