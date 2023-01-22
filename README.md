```
$ git clone git@github.com:levalves/docker-sample-api.git

$ docker image build -t docker-api:1.0 .

$ docker image ls
REPOSITORY            TAG       IMAGE ID       CREATED        SIZE
levalves/docker-api   1.0       0cddbef9f6bf   24 hours ago   254MB

$ docker tag docker-api:1.0 levalves/docker-api:1.0

$ docker container run -p 8080:3000 -d --name docker-api levalves/docker-api:1.1 

$ docker image ls
REPOSITORY   TAG            IMAGE ID       CREATED              SIZE
docker-api   1.0            0cddbef9f6bf   About a minute ago   254MB
node         current-slim   91d9ac08181c   10 days ago          248MB

$ docker login -u "username" -p "mypassword" docker.io

$ docker push levalves/docker-api:1.0
```

Acessar https://hub.docker.com e verificar o novo repositório criado
