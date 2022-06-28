### Class 1 - Imagens e containers

### Comandos interessantes:

`docker ps -a` 

=> 

ps = processos

-a = all

`docker run -p LOCAL_PORT:INTERNAL_DOCKER_CONTAINER_EXPOSE_PORT IMAGE` 

=> 

LOCAL_PORT: Porta local, exemplo 3000

INTERNAL_DOCKER_CONTAINER_EXPOSE_PORT = Porta exposta no Dockerfile 

IMAGE = Código da image gerada na build

### Flags interessantes:

`docker run -d IMAGE` de detached => Cria um container baseado em uma `IMAGE` de maneira `detached`, ou seja, não trava o terminal e não mostra os logs enquanto o terminal estivesse aberto

`docker attach container` => Depois de iniciar um container em forma `detached`, é possível ficar de maneira `attached` novamente com esse comando

`docker start -a CONTAINER` de attached => Inicia um `CONTAINER` que estava parado de maneira `attached` para que seja possível visualizar os futuros logs vindo no terminal enquanto este comando estiver rodando.

`docker logs CONTAINER` => Mostra todos os logs daquele container, inclusive enquanto estava de maneira `detached`

`docker logs -f CONTAINER` de follow => Continua mostrando os logs daquele container, como se estivesse de maneira `attached`

Observações:

A forma padrão de rodar o `docker run` é de maneira `attached`

A forma padrão de rodar o `docker start` é de maneira `detached`
