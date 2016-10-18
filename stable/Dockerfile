## Get latest stable NeuroDebian image
FROM ubuntu:yakkety

RUN apt-get update
RUN apt-get install -y \
	dirmngr \
	wget
RUN echo "deb http://neuro.debian.net/debian wheezy main" >>  /etc/apt/sources.list.d/neurodebian.sources.list
RUN echo "deb http://neuro.debian.net/debian data main" >>  /etc/apt/sources.list.d/neurodebian.sources.list
RUN echo "deb http://us.archive.ubuntu.com/ubuntu trusty main universe" >>  /etc/apt/sources.list.d/neurodebian.sources.list
RUN echo "deb http://us.archive.ubuntu.com/ubuntu wily main universe" >>  /etc/apt/sources.list.d/neurodebian.sources.list

RUN wget -O- http://neuro.debian.net/lists/wily.us-tn.full | tee /etc/apt/sources.list.d/neurodebian.sources.list \
 && apt-key adv --recv-keys --keyserver hkp://pgp.mit.edu:80 0xA5D32F012649A5A9

RUN apt-get update

## Install afni
##RUN apt-get install -y \
##	libgsl0ldbl \
##	libnetcdf7 \
##	afni \
##	fsl-complete
