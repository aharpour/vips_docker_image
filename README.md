## Overview
A base Ubuntu 15.04 with a number of image manipulation libraries. This image was particularly built to run in Iron.io's IronWorker framework, allowing for mass parallel of processing of image data.

## Requirments
You are going to need [Docker](https://www.docker.com/) installed. You can find a variety of installation instructions, per operating system, in the [Docker Installation Docs](https://docs.docker.com/installation/#installation). If you haven't used Docker before, take a moment and look through the [Docker User Guide](https://docs.docker.com/userguide/).

## Pull The Docker Repository
`docker pull bubba/vips-docker-image`

## In the Image
Library     | Versions
------------|---------
Python      | 2.7.9 
PHP         | 5.6.4 
vips        | 8.0.2 
pdfinfo     | 0.30.0
ghostscript | 9.15

### Build Notes
Vips 8.0.2 was built in the image and all other libraries were installed via the apt-get package manager. There are also a handful of PHP and Python libraries/modules installed as well, please see the Dockerfile for more details.

## Command Line Usage
Assuming you have a directory `/tmp/docktest` that contians an image `/tmp/docktest/bbq.jpg` and you want to use this contianer to convert the image to thumbnail, you might run this command:

```docker run -ti --rm  -v /tmp/docktest:/mnt/vips -w /mnt/vips bubba/vips-docker-image vipsthumbnail bbq.jpg --size 200x100```

and discover `/tmp/docktest/tn_bb1.jpg` has been created. 
