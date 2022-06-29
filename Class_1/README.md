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

`docker run -it IMAGE` de terminal interativo => Cria um container baseado em uma `IMAGE` de maneira que permita esse container usar um terminal interativo, para aplicações que necessitem de inputs de usuário

`docker start -ai CONTAINER` de attached e interativo => Inicia um `CONTAINER` de maneira que possa interagir de maneira iterativa, que necessite de inputs do usuário

`docker run --rm IMAGE` de remove (detalhe que são 2 --) => Remove o container que for iniciado a partir da `IMAGE` depois que ele for parado automaticamente

`docker run --name NOME_DO_CONTAINER IMAGE` => Dá um nome para o container criado a partir da `IMAGE`

`docker build -t NOME:TAG .` => Cria uma image com `NOME` e `TAG` definidas. 
Obs: `NOME` pode ser chamado também de `REPOSITORY`

Observações:

A forma padrão de rodar o `docker run` é de maneira `attached`

A forma padrão de rodar o `docker start` é de maneira `detached`
