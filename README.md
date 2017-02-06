# zeta-Docker

This project helps you to setup zeta.

## Setup

First check this repository out. After that checkout the zeta/modigen repository. And copy it as modigen-v3 into zeta-docker or you could just adjust the docker-compose.yml and write in your own paths.

```
git clone https://github.com/HTWG-VirtualReality/zeta-docker.git
cd zeta-docker
git clone https://bitbucket.org/mgerhart/modigen-v3.git
cd modigen-v3/server/public
git clone https://github.com/HTWG-VirtualReality/prototyp.git
docker run -it --rm -v "$PWD/prototyp":/usr/src/app -w /usr/src/app node:6 /bin/bash -c "npm install -g bower; bower install --allow-root"
```

Besides these step you should also have ```docker``` and ```docker-compose``` installed.

## Usage

Just execute ```docker-compose up``` within zeta-docker folder and the containers gets started. Only at the first execution it will take very long (ca. 20-30 min) for retrieving all dependencies.

## Login

Automatic created users with their passwords can be found in```modigen-v3/server/app/models/SecureSocialUser.scala```.
Call http://localhost:9000/oauth/setup after the first login to create necessary oauth credentials.
