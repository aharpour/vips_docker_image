## Overview
A base Ubuntu 15.04 with a number of image manipulation libraries. This image was particularly built to run in Iron.io's IronWorker framework, allowing for mass parallel of processing of image data.

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

## Build Notes
Vips 8.0.2 was built in the image and all other libraries were installed via the apt-get package manager. There are also a handful of PHP and Python libraries/modules installed as well, please see the Dockerfile for more details.


