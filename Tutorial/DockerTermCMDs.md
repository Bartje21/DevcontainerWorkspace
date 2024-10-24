# Docker Terminal Commands

### *Run Docker container*

`docker run --name AppName-container -p 80:80 DockerImage`

### *Run Docker Container in detached mode (-d)*

`docker run --name AppName-container -p 80:80 -d DockerImage`

### *View a summary of image vulnerabilities and recommendations*

`docker scout quickview`

### *Remove Devcontainer*

`docker rm AppName-container`

### *View Active Containers/Ports*

`docker ps`