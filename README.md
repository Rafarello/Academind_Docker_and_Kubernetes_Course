### Class 1 - Imagens e containers

Comandos interessantes:

`docker ps -a` 

=> 

ps = processos

-a = all

`docker run -p LOCAL_PORT:INTERNAL_DOCKER_CONTAINER_EXPOSE_PORT IMAGE` 

=> 
LOCAL_PORT: Porta local, exemplo 3000

INTERNAL_DOCKER_CONTAINER_EXPOSE_PORT = Porta exposta no Dockerfile 

IMAGE = Código da image gerada na build
