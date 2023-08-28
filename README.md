
```sh
$ docker network create traefik-public
$ docker-compose -f docker-compose.traefik.yml up -d
# dev
$ docker-compose -f docker-compose.yml up -d

# prod
$ docker network create traefik-public
$ docker-compose -f docker-compose.traefik.prod.yml up -d
$ docker-compose -f docker-compose.prod.yml up -d
```


# Dockerizing FastAPI with Postgres, Uvicorn, and Traefik

## Want to learn how to build this?

Check out the [post](https://testdriven.io/blog/fastapi-docker-traefik/).

## Want to use this project?

### Development

Build the images and spin up the containers:

```sh
$ docker-compose up -d --build
```

Test it out:

1. [http://fastapi.localhost:8008/](http://fastapi.localhost:8008/)
1. [http://fastapi.localhost:8081/](http://fastapi.localhost:8081/)

### Production

Update the domain in *docker-compose.prod.yml*, and add your email to *traefik.prod.toml*.

Build the images and run the containers:

```sh
$ docker-compose -f docker-compose.prod.yml up -d --build
```
