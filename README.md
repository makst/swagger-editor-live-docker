# Swagger editor live docker

Dockerfile, based on [moon0326/swagger-editor-live](https://github.com/moon0326/swagger-editor-live)
npm package. It's a live swagger editor that saves your changes back to the file.

# Usage

## CLI

```
$ docker run -it -e EDITOR_PORT=3001 -p 3001:3001 -v /local/path/to/swagger.yml:/swagger.yml makst/swagger-editor-live-docker
```

## Docker compose
```
version: '3.4'

services:
    swagger-editor:
        image: makst/swagger-editor-live-docker
        environment:
            - EDITOR_PORT=3001
        volumes:
            - /local/path/to/swagger.yml:/swagger.yml
        ports:
            - "3001:3001"
```
