# backend
Backend prototype


## Install

Make sure you have these tools installed before you start:
- Docker and Docker Compose
- ngrok

If you are in a Mac:

```shell
brew cask install docker
brew cask install ngrok
```


## Quick start

Start Elasticsearch

```shell
docker-compose up -d
```

Open a tunnel so that people can send requests to the Elasticsearch instance

```shell
ngrok start --config=ngrok.yml elasticsearch
```
