### Docker commands
    - docker -v/--version --> pegar a versão do docker
    - docker image ls --> listar imagens
    - docker image ls nome-container --> listar imagem especifica
    - docker image rm --> remover imagens
    - docker image history api-rocket --> listar hisrico image
    - docker container ls --> listar container
    - docker container inspect id_container => Inspeciona o container

    - docker build -t api-rocket . --> Criar container
    - docker build -t api-rocket:v1 . --> Criar container passando uma tag
    - sudo docker run --rm -p 3000:3000 api-rocket --> rodar container (--rm => garante a efêmeridade do container apagando-a quando encerra o container -p 3000:3000 configuração da porta.)
    - docker ps -> ver os container que estão rodando
    - sudo docker run -p 3001:3000 -d api-rocket => roda container em background.
    - docker stop id
    - docker start id
    - docker container prune => Remove unused container
    - docker image prune => Remove unused image
    - docker image prune -a => Remove unused image
    - docker volume prune => Remove unused volumes
    - docker network prune => Remove unused networks
    - docker rm $(docker ps -aq) => remove todos os conteineres não usados
    - docker logs id_container => Para visualizar os logs de um container


rm -rf .git*

### Redes e volumes
    Camada de abtração
    - docker network
    - sudo docker network create network-api-rocket => Criar novo network
    - sudo docker network create --driver (bridge || host) network-api-rocket => Criar novo network passando um driver manualmente.
    - sudo docker network connect (3e8f7f458c4a => id network) (c364c7d0437d => id container) => conecta o network ao container.
    - sudo docker network inspect 3e8f7f458c4a => Inspeciona o network
    - sudo docker run --network=network-api-rocket -p 3001:3000 -d api-rocket - Roda container passando o network

    Volumes - Arquivos e Containers
    x - Permite persistir dados.
    - sudo docker exec -it e61ccb466e55 bash => visualizar app que está dentro do container
    - sudo docker volume
        - create => Create a valume
        - inspect => Display detailed information
        - ls
        - prune
        - rm
    
    docker run -v volume-api-rocket:/usr/src/app --network=network-api-rocket -p 3001:3000 -d api-rocket => rodando container criando volume

### Melhorando a performance
    Alpine e Stretch
        - Os alpine são imagens mais seguros e mais leves.
    
    Criando múltiplos estágios
        - 

### Roadmap de configuração dockerfile para um projeto nestjs
    1. node instalado
    2. yarn || npm install
    3. yarn || npm run build
    4. yarb || npm run start

### Notes
    - Tipos de image
    (slim, alpines e completos).