# CMIS Docker  
This repository contains a ready-to-use version of PSYMBIOSYS CMIS Knowledge Browser for Docker.  

## Content  
The components inside the repository are listed below:

- **images**: This folder contains the docker volumes definition of all the components related to PSYMBIOSYS CMIS Knowledge Browser.  
	- **alfresco**: volume related to Alfresco Docker Image.
	- **db_data**: volume related to the MySql Docker Image.
	- **nlp_batch**: contains the [Dockerfile](images/nlp_batch/Dockerfile) needed for the creation of a Docker Image. This Docker Image stores and launches the NLPBatch .
	- **tomcat**: replicates the installation directory of Apache Tomcat, in which is possible to deploy web applications in the form of ".war" files [Data](images\tomcat\war) folder.
	- **virtuoso**: volume related to the Virtuoso Docker Image.
- **docker-compose.yml**: YAML file used to start the entire System.

## Usage  
Download the latest version of Docker from its website and start it. After the correct configuration of CMIS Knowledge Browser, through the command line move into the folder already downloaded and locally stored; type the following command:

`docker-compose up`

This command will automatically start all the services.  

> **Note:** For more details about the usage and the configuration, visit [OGJira GitHub Repository](https://github.com/FINCONS-IBD/CMIS)