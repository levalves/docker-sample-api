```
$ git clone git@github.com:levalves/docker-sample-api.git

$ docker image build -t docker-api:1.0 .

$ docker image ls
REPOSITORY   TAG            IMAGE ID       CREATED              SIZE
docker-api   1.0            0cddbef9f6bf   About a minute ago   254MB
node         current-slim   91d9ac08181c   10 days ago          248MB

$ docker container run -p 8080:3000 -d --name docker-api levalves/docker-api:1.1 

$ docker container ls
CONTAINER ID   IMAGE                     COMMAND                  CREATED        STATUS        PORTS                                                 NAMES
d6147e018ab6   levalves/docker-api:1.0   "docker-entrypoint.s…"   22 hours ago   Up 1 second   8080/tcp, 0.0.0.0:8080->3000/tcp, :::8080->3000/tcp   docker-api

$ docker tag docker-api:1.0 levalves/docker-api:1.0

$ docker login -u "username" -p "mypassword" docker.io

$ docker push levalves/docker-api:1.0
```

Acessar https://hub.docker.com e verificar o novo repositório criado
