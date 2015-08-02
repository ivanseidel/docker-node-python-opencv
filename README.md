docker-node-python-opencv
=============

Node.js, Python and OpenCV for Python on Docker.

First install docker on your computer 

http://docs.docker.io/en/latest/installation/ubuntulinux/

and clone the repo, and enter the following command:

```
sudo docker build .
```

and you are ready to go!

you can also pull the docker image from [index.docker.io](http://index.docker.io)

https://index.docker.io/u/ivanseidel/node-python-opencv/

```
sudo docker pull ivanseidel/node-python-opencv
```

and your docker is set!

### Fixing libdc1394 error

Note that this Dockerfile fixes the error `libdc1394 error: Failed to initialize libdc1394` by running 
the link command on startup. In case you need another command, and want to keep python working with OpenCV
without errors, use:

`CMD sh -c 'ln -s /dev/null /dev/raw1394'; <your-script-here>`

[Stack Overflow thread](http://stackoverflow.com/a/31769286/1234504)

