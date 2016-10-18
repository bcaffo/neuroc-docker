## Get latest stable NeuroDebian image
FROM neurodebian:latest

## Download the package lists from the repositories 
## and update them to get information on the newest 
## versions of packages and their dependencies
RUN apt-get update

## Install pgp keys (otherwise neurodebian packages will fail to install)
RUN apt-get install -y gnupg2 gnupg

RUN wget -O- http://neuro.debian.net/lists/sid.us-tn.full | tee /etc/apt/sources.list.d/neurodebian.sources.list \
&& apt-key adv --recv-keys --keyserver hkp://pgp.mit.edu:80 0xA5D32F012649A5A9

## Install AFNI, fsl
RUN apt-get install -y \
	afni \
	fsl-complete
