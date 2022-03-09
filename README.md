# Getting started

## What is this?

This is a basic getting started template of sorts to get Jupyter up and running on any machine that can run `docker` and `docker-compose`.

## How to get it up and running

We will assume that you have `docker` and `docker-compose` setup on your machine. If not, follow the instructions listed here: [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)


### Running `docker-compose up`

In your current directory, run the following command:

```sh
$ docker-compose up
```

Acquire and go to the link with the attached token in the command line:

![image](https://user-images.githubusercontent.com/1130103/157421053-f6f8ad7a-d9c4-48e4-8c2a-386c748edd0e.png)

---
### Running `docker-compose up -d`

In the case you want to run this command detached from your terminal, you can run:

```sh
$ docker-compose up -d
```

You can then access the container to list out the Jupyter servers:
```
$ docker exec -it getting-started-datascience-notebook bash
$ jupyter server list
```

Make sure to replace the generated DNS link from the container's id (in our case `cae8c1fde086`) with `localhost`.

![image](https://user-images.githubusercontent.com/1130103/157423029-eceb9409-6232-479a-9682-82abcb9f210e.png)

When you are able to access through the link, you will (hopefully) see this page.

![image](https://user-images.githubusercontent.com/1130103/157424277-e4b8a10f-4b93-4f94-8707-dac3c90d4386.png)

## Extending the docker image

You can view the recipes page for Jupyter docker stacks to get an idea of how to extend the docker image to a build file: [https://jupyter-docker-stacks.readthedocs.io/en/latest/using/recipes.html](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/recipes.html)

#TODO add dockerfile + edit docker-compose.yaml to include manual builds for custom libraries.
