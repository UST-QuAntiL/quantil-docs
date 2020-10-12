# QuAntiL Docker setup
This section explains how to execute the complete QuAntiL environment with docker-compose.

## Overview
The following components are included in the docker-compose setup

| QuAntiL Component | URL | GitHub | Docker Hub |
|:------------------- |:--- |:------ |:---------- |
| Postgres-Multi DB | <localhost:5432> | [Link](https://github.com/lmm-git/docker-postgres-multi) | [Link](https://hub.docker.com/r/lmmdock/postgres-multi) |
| QC-Atlas |<http://localhost:8080/atlas> | [Link](https://github.com/UST-QuAntiL/qc-atlas) | [Link](https://hub.docker.com/r/planqk/atlas) |
| QC-Atlas-UI |<http://localhost:4200> | [Link](https://github.com/UST-QuAntiL/qc-atlas-ui) | [Link](https://hub.docker.com/r/planqk/qc-atlas-ui) |
| Pattern-Atlas-API |<http://localhost:8082/patternpedia> | [Link](https://github.com/PatternAtlas/pattern-atlas-api) | [Link](https://hub.docker.com/r/patternpedia/patternrepo-api) |
| NISQ-Analyzer |<http://localhost:8081/nisq-analyzer> | [Link](https://github.com/UST-QuAntiL/nisq-analyzer) | [Link](https://hub.docker.com/r/planqk/nisq-analyzer) |
| Qiskit-Service |<http://localhost:5000> | [Link](https://github.com/UST-QuAntiL/qiskit-service) | [Link](https://hub.docker.com/r/planqk/qiskit-service) |
| Redis |<localhost:6379> | [Link](https://github.com/redis/redis) | [Link](https://hub.docker.com/_/redis) |

## Prerequisites
- Docker Engine - [install guide](https://docs.docker.com/engine/install/)
- Docker Compose - [install guide](https://docs.docker.com/compose/install/)
- The [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker)

**Make sure following ports in your environment are free in order to start the QuAntiL environment properly:**

* `8080`-`8082`
* `5432`
* `5000`
* `4200`
* `6379`

## Running the complete setup
Make sure all prerequisites above are met bevorhand and that all necessary ports are free.

1. Navigate inside the root directory of the [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker)
2. Execute `docker-compose pull` - pulls the most recent version of all images
3. Execute `docker-compose up -d` - starts all services in the background

To check if everything is running correctly use the command `docker ps -a` for a list of all running containers and their corresponding containerIds.
The logs of each individual container can be viewed by executing `docker logs <containerId>`.

To stop every service simply execute `docker-compose down`.

## Running only selected services
Sometimes only a subset of the provided images is needed to save computing resources or for development purposes. E.g. the database is running inside the container but IntelliJ is executing qc-atlas.
This is achieved by following the steps above, but instead of executing the command in step 3, use the command 
`docker-compose up -d <serviceName1> <serviceName2> ... <serviceNameN>` 
where each `<serviceNameX>` is replaced by the desired service names. 
E.g. `docker-compose up -d db qc-atlas` executes the database service and the `qc-atlas` backend. However, keep in mind that some services heavily depend on each other and may not work properly if dependent services are not running.

## Import Example Data
Data from the [pattern-atlas-content](https://github.com/PatternAtlas/pattern-atlas-content) repository will always be imported automatically.
However, to import example data from the [qc-atlas-content](https://github.com/UST-QuAntiL/planqk-atlas-content) and [nisq-analyzer-content](https://github.com/UST-QuAntiL/nisq-analyzer-content) repositories make sure to follow these steps:

1. Rename the `docker-compose.override.yml` file inside the [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker) to `docker-compose.override.yml`.
2. Provide a ssh private key file with correct access rights for the [qc-atlas-content](https://github.com/UST-QuAntiL/planqk-atlas-content) repository. The file has to be called `ssh_secret` and is located in the root folder of the [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker).
3. It is required that the data directory is empty before starting the container to prevent the deletion of data, see [postgres-docker documentation](https://github.com/docker-library/docs/tree/master/postgres#initialization-scripts).

### FAQ

##### How do I make sure that all necessary ports are free?
Windows: `netstat -anp | find ":<portNumber>"` - shows processes listening on <portNumber>
Linux: `sudo lsof -i -P -n | grep LISTEN` - shows all processes listening any port
OSX: `netstat -anp tcp | grep LISTEN` for tcp and `netstat -anp udp | grep LISTEN for udp`

##### Why is the example data not imported?
Make sure you followed the instructions above. If you still experience problems follow these steps:

1. Execute `docker-compose rm -f` - **this removes all containers and volumes**
2. Run `docker-compose pull` - pull all images
3. Execute `docker-compose up --build -d` - this rebuilds all services and starts them

##### How do I use a local repository and build the image myself?
Depending on the service you want to build yourself from a local repository change the image name and add a new build context to the service inside the docker-compose file. E.g.
```
...
<serviceName>:
  build:
    context: <repoLocation>
  image: <imageName>
...
```
`<serviceName>` - represents the name of the service
`<imageName>` - represents the new name of the image.
`<repoLocation>` - represents the location of the repository relative to the directory of the `docker-compose.yml` file. The location has to contain the `Dockerfile` of the service.

##### Where do I get a ssh private key file with the correct access rights?
Follow the [documentation of Github](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh) to generate and add the ssh key to your Github account. The generated private key is the file you need, do not share this file with anyone.