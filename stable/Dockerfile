## Get latest stable NeuroDebian image
FROM neurodebian:latest

## Download the package lists from the repositories 
## and update them to get information on the newest 
## versions of packages and their dependencies
RUN apt-get update

## Install AFNI
RUN apt-get install -y \
	afni \
	fsl-complete
