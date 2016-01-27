# Hands' On Text Mining

Hands' on presentation on Text Mining. Exercices and solutions are available in notebooks both in Scala and Python.

## Building a docker image

If you do not have notebooks configurations installed in your computer, you can build the docker image associated to the language of your choice. The commands given as examples were run in a MacBook, please go on [docker's website](https://docs.docker.com/installation/) to install docker on your OS before running the following commands.

### In Python

To build the docker jupyter pyspark-notebook image, run the following lines into your docker terminal:

```
cd python
docker build -t pyspark-notebook .
docker run -d -p 8888:8888 -v /your/path/xke-text-mining/python/:/home/joyvan/work pyspark-notebook
```