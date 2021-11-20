# Docker Commands
| Commands | Description |
| ----------- | ----------- |
| docker ps| list all active containers |
| docker ps -a  | list all active and terminated containers |
| docker image ls | list all images |
| docker rm `<<container_name>>` | removing container |
| docker run -d -p 8080:8010 `<<image name>>` | starting the container with detach(-d) mode with port mapping 8080 exposed outside and 8010 port the container runnning inside the docker|
| docker stop `<<container_name>>` | stopping container  |
| docker start `<<container_name>>` | starting the container |
| docker logs `<<container_name>>` | viewing the logs of the container |