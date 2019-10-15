# TIS - Readme

## Content

- 00-Setup : file for docker image generation,
- 01-Labs(Tex) : Latex files for Labs,
- 03-Labs(Matlab) : Matlab solution of Labs,
- 04-Labs(Python) : Solution of labs in Python,
- 05-Labs(Templates Python) : Templates of labs for students.


## Start the jupyter lab

To start the Jupyter lab environment, run the following command in a Terminal:

For MKR:
``docker run...``

For PBR:

``/usr/local/bin/docker run -p 8888:8888 -v /Users/pierre/Documents/01-HEIG-VD/11-COURS/TIS/:/home/tis 314rch/tislab``


## Generate the docker IMAGE

Change directory to the docker place:

``cd /Users/pierre/Documents/01-HEIG-VD/11-COURS/TIS/00-Setup/docker``

Edit the ``dockerfile`` file and apply the needed changes.

Build the image:

``docker build .``

Get the image ID through the followin command:

``docker image ls``

Tag the image:

``docker tag <imgaeId> 314rch/tislab``

After validation, push it to ``dockerhub``

```
> docker login --username=314rch
```

```
> docker push 314rch/tislab
```
