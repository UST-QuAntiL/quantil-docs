# Quickstart with QuAntiL Docker setup
This section explains how to execute the QuAntiL components supported by the QC Atlas UI with docker-compose.

## Prerequisites
- Docker Engine - [install guide](https://docs.docker.com/engine/install/)
- Docker Compose - [install guide](https://docs.docker.com/compose/install/)
- The [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker)

## Overview
The following components are included in the docker-compose setup

| QuAntiL Component | URL | GitHub | Docker Hub |
|:------------------- |:--- |:------ |:---------- |
| QC-Atlas-UI |<http://localhost:80> | [Link](https://github.com/UST-QuAntiL/qc-atlas-ui) | [Link](https://hub.docker.com/r/planqk/qc-atlas-ui) |
| QC-Atlas |<http://localhost:6626/atlas> | [Link](https://github.com/UST-QuAntiL/qc-atlas) | [Link](https://hub.docker.com/r/planqk/atlas) |
| Pattern-Atlas-API |<http://localhost:1977/patternatlas> | [Link](https://github.com/PatternAtlas/pattern-atlas-api) | [Link](https://hub.docker.com/r/patternatlas/pattern-atlas-api) |
| Pattern-Atlas-UI |<http://localhost:1978> | [Link](https://github.com/PatternAtlas/pattern-atlas-ui) | [Link](https://hub.docker.com/r/patternatlas/pattern-atlas-ui) |
| NISQ-Analyzer |<http://localhost:5010/nisq-analyzer> | [Link](https://github.com/UST-QuAntiL/nisq-analyzer) | [Link](https://hub.docker.com/r/planqk/nisq-analyzer) |
| Quantum-Transpiler-Frontend |<http://localhost:5011> | [Link](https://github.com/UST-QuAntiL/QuantumTranspiler) | [Link](https://hub.docker.com/r/planqk/quantum-transpiler-frontend) |
| Quantum-Transpiler-Backend |<http://localhost:5012> | [Link](https://github.com/UST-QuAntiL/QuantumTranspiler) | [Link](https://hub.docker.com/r/planqk/quantum-transpiler-backend) |
| Qiskit-Service |<http://localhost:5013> | [Link](https://github.com/UST-QuAntiL/qiskit-service) | [Link](https://hub.docker.com/r/planqk/qiskit-service) |
| Forest-Service |<http://localhost:5014> | [Link](https://github.com/UST-QuAntiL/forest-service) | [Link](https://hub.docker.com/r/planqk/forest-service) |
| Pytket-Service |<http://localhost:5015> | [Link](https://github.com/UST-QuAntiL/pytket-service) | [Link](https://hub.docker.com/r/planqk/pytket-service) |
| Rigetti QVM |<http://localhost:5016> | [Link](https://github.com/rigetti/qvm) | [Link](https://hub.docker.com/r/rigetti/qvm) |
| Rigetti Quilc |<http://localhost:5017> | [Link](https://github.com/rigetti/quilc) | [Link](https://hub.docker.com/r/rigetti/quilc) |
| Cirq-Service |<http://localhost:5018> | [Link](https://github.com/UST-QuAntiL/cirq-service) | [Link](https://hub.docker.com/r/planqk/cirq-service) |
| Braket-Service |<http://localhost:5019> | [Link](https://github.com/UST-QuAntiL/braket-service) | [Link](https://hub.docker.com/r/planqk/braket-service) |
| QProv |<http://localhost:5020/qprov> | [Link](https://github.com/UST-QuAntiL/qprov) | [Link](https://hub.docker.com/r/planqk/qprov) |
| QProv-Collector-IBM |<http://localhost:5021> | [Link](https://github.com/UST-QuAntiL/qprov) | [Link](https://hub.docker.com/r/planqk/qprov-collector) |
| QSharp-Service |<http://localhost:5022> | [Link](https://github.com/UST-QuAntiL/qsharp-service) | [Link](https://hub.docker.com/r/planqk/qsharp-service) |
| Latex-Renderer |<http://localhost:5030> | [Link](https://github.com/UST-QuAntiL/latex-renderer) | [Link](https://hub.docker.com/repository/docker/planqk/latex-renderer) |
| Redis |<http://localhost:5040> | [Link](https://github.com/redis/redis) | [Link](https://hub.docker.com/_/redis) |
| Postgres-Multi DB | <tcp://localhost:5060> | [Link](https://github.com/lmm-git/docker-postgres-multi) | [Link](https://hub.docker.com/r/lmmdock/postgres-multi) |
| Config-Server |<http://localhost:2379> | [Link](https://github.com/etcd-io/etcd) | [Link](https://quay.io/repository/coreos/etcd) |
| PlanQK Library              |<http://localhost:2903>                | [Link](https://github.com/UST-QuAntiL/PlanQK-Library)      | [Link](https://hub.docker.com/repository/docker/planqk/planqk-library)   

**Make sure following ports in your environment are free in order to start the QuAntiL environment properly:**

* `80`
* `1977`
* `1978`
* `2379`
* `2903`
* `5010`-`5022`
* `5030`
* `5040`
* `5060`
* `6626`

Thereby, [QC Atlas](../user-guide/qc-atlas.md) builds the basic knowledge base. The different additional features of [NISQ Analyzer](../user-guide/nisq-analyzer.md), [Pattern Atlas](../user-guide/qc-atlas/pattern-relation-type.md), and [QProv](../user-guide/qprov.md) are supported on top of the QC Atlas and are defined as feature sets.  

##### The defined feature sets are namely:
- `all` (runs all features)  
- `nisqAnalyzer`  
- `nisqAnalyzerCompilerComparison`  
- `patternAtlas`  
- `qprov`  

## Running the QuAntiL components supported by the QC Atlas UI
Make sure all prerequisites above are met beforehand and that all necessary ports are free.
Then, navigate inside the root directory of the [quantil-docker repository](https://github.com/UST-QuAntiL/quantil-docker).

### Running the base components
The base components [QC Atlas](../user-guide/qc-atlas.md), QC Atlas UI, [LaTeX Renderer](../user-guide/qc-atlas/latex-renderer.md), Config-Server, and the databases without any of the named features run by default using:

1. Execute `docker-compose pull` - pulls the most recent version of the images
2. Execute `docker-compose build db`
3. Starting the DB first: `docker-compose up -d db`
4. Execute `docker-compose up -d` - starts all remaining services in the background

To check if everything is running correctly use the command `docker ps -a` for a list of all running containers and their corresponding containerIds.

The logs of each individual container can be viewed by executing `docker logs <containerId>`.

To stop every service simply execute `docker-compose down -v`. 
`-v` ensures that all volumes are removed (if example data is imported - see next section - this can be crucial)

### Running certain feature sets
For running certain [feature sets](#the-defined-feature-sets-are-namely) on top of the base components, [Profiles](https://docs.docker.com/compose/profiles/) are used.  
To start a certain feature set run:  
`docker-compose --profile <name-of-feature-set> pull`  
`docker-compose --profile <name-of-feature-set> up`

For running multiple feature sets, e.g. two sets, run:  
`docker-compose --profile <name-of-feature-set-1> --profile <name-of-feature-set-2> pull`  
`docker-compose --profile <name-of-feature-set-1> --profile <name-of-feature-set-2> up`
  
For running all feature sets, choose `--profile all`.

### Running only selected services
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


## FAQ

##### How do I make sure that all necessary ports are free?
Windows: `netstat -anp | find ":<portNumber>"` - shows processes listening on <portNumber>

Linux: `sudo lsof -i -P -n | grep LISTEN` - shows all processes listening any port

OSX: `netstat -anp tcp | grep LISTEN` for tcp and `netstat -anp udp | grep LISTEN for udp`


##### Why is the example data not imported?

- Are the line-endings configured correctly? 
`/docker-entrypoint-initdb.d/setup-atlas.sh: line 2: cd: $'/var/qc-atlas/testdata\r': No such file or directory` in the db logs indicates that LF is not used as line-endings. In IntelliJ, you can override this setting via choosing File > File Properties > Line Separators > LF 

- Make sure you followed the instructions above. If you still experience problems follow these steps:

1. Execute `docker-compose rm -vf` - **this removes all containers and volumes**
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
