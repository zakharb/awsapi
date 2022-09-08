
![logo](logo.png)

## AWS API  
### Micro services in AWS Services  


![](https://img.shields.io/badge/version-1.0-blue)
![](https://img.shields.io/badge/python-3.9-blue)

## Content  
[Important info](#important_info)  
[Install](#install)  
[Configuration](#configuration)  
[Client](#client)  
[Usage](#usage)  


<a name="important_info"/>

## Important info  
</a>  

> AWS API work as fully separates API in Async mode  
> Stack: FastAPI + React + Nginx + Postgres  
> Each Service run in docker containers   
> Easily expandability With Micro Service architecture  
> DB located in AWS RDS
> Database can be easily switch from Postgres to MongoDB or other  

<a name="install"/>  

## Install  
</a>  

- Create EC2 instances
- Login to it via SSH
- Install `docker` and `docker-compose`  
- Clone repo  
- Create RDP instance
- Change DATABASE_URI parametr in docker-compose.yml
- Run `docker-compose up -d`   

<a name="configuration"/>  

## Configuration  
</a>  

> To solve problem with performance each Service run in container  
> Uvicorn work as ASGI server and connect to one piece with Nginx  
> Main configuration is `docker-compose.yml`  

- every service located in separate directory `name-service`  
- use `Dockerfile` to change docker installation settings  
- folder `app` contain FastAPI application  
- all services connected to one piece in `docker-compose.yml`  


<a name="client"/>  

## Client UI  
</a>  

- UI is available via URI `http://ec2-dns-name.amazonaws.com:8080/tickets`   

