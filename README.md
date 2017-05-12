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
ngrok start --subdomain=dearmayor --config=ngrok.yml elasticsearch
```

## Initializing ES
```shell
curl -XPUT 'localhost:9200/dearmayor?pretty' -H 'Content-Type: application/json' -d@mapping.json
curl -XPOST 'localhost:9200/dearmayor/dearmayor/?pretty' -H 'Content-Type: application/json' -d@demo1.json
curl -XPOST 'localhost:9200/dearmayor/dearmayor/?pretty' -H 'Content-Type: application/json' -d@demo2.json
curl -XPOST 'localhost:9200/dearmayor/dearmayor/?pretty' -H 'Content-Type: application/json' -d@pict.json
```

