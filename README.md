# Hands' On Text Mining

Hands' on presentation on Text Mining. Exercices and solutions are available in notebooks both in Scala and Python.

## Building a docker image and Running a container

If you do not have notebooks configurations installed in your computer, you can build the docker image associated to the language of your choice. The commands given as examples were run in a MacBook, please go on [docker's website](https://docs.docker.com/installation/) to install docker on your OS before running the following commands.

### In Python

To build the docker jupyter pyspark-notebook image, run the following lines into your docker terminal:

```
cd /your/path/xke-text-mining/python/
docker build -t pyspark-notebook .
docker run -d -p 8888:8888 -v /your/path/xke-text-mining/python/:/home/joyvan/work pyspark-notebook
```

This will run a docker container with all requirements to work on pyspark notebooks.

### In Scala

To build the docker datafellas scala-spark-notebook image, run the following lines into your docker terminal:

```
cd /your/path/xke-text-mining/scala/
docker build -t scala-spark-notebook .
docker run -d -p 9000:9000 -v /path/:/opt/docker/notebooks/ scala-spark-notebook
```

This will run a docker container with all requirements to work on spark notebooks with scala.

## Working with notebooks

Once you have run the contained associated with the language of your choice, all you need is to open your browser and open the page corresponding to your default ip address and the selected port.

To get your default ip address (on MacBook, with docker-machine):

```
docker-machine ip default
```

Then, in your browser, enter the selected ip address with the associated port (ip:8888 in Python, ip:9000 in scala for this exercice).

Your can then go the the notebooks directory and start working on the exercice notebook. A notebook with some proposed solutions is also available.

## Additionnal useful docker commands

* Show all available images on your computer: `docker images`
* Show information on the running container: `docker ps`
* Stop a container: `docker stop container_id`
* Remove an image from your computer: `docker rmi -f image_id`

You may eventually have to check your default VM size on VirtualBox (4GB is a good size). No other knowledge of docker is required to complete the exercices.

## About the exercices

In the exercices, you will be working on processing articles from [Xebia's blog](https://docs.docker.com/installation/) since 2014. The goal is to introduce the user to some useful techniques and algorithms when working on text data.