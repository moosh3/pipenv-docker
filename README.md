# pipenv-docker

[![](https://images.microbadger.com/badges/version/aleccunningham/pipenv.svg)](https://microbadger.com/images/aleccunningham/pipenv "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/aleccunningham/pipenv.svg)](https://microbadger.com/images/aleccunningham/pipenv "Get your own image badge on microbadger.com")

## Installation 

```
$ docker pull aleccunningham/pipenv:3.6-onbuild
```

## Usage

This dockerfile is structured to be used as a base image for a python 3.6 application. When paired with your application, it should look similar to the following.

```
FROM aleccunningham/pipenv:3.6-onbuild

COPY . /app

RUN python3 main.py
```

Making use of the `ONBUILD` command allows for docker to automagically add and install dependencies defined in a `Pipfile`. 
