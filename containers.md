## Containers e Dockers
    - [O que é?]([text](https://www.redhat.com/pt-br/topics/containers/what-is-docker))
     - Ambiente isolado.
    - Compartilha um host
    - Contém todos os elementos necessários para rodar uma aplicação
    - LXC - Linux containers

### Máquinas virtuais
    - Tudo roda na mesma máquina
    - Possui seu próprio SO

### Docker
    - Surgiu há cerca de 15 anos (+/- 2003)
    - Interface para lidar com containers
    - Utiliza o kernel do linux
    - Baseado em imagem
    - Facilita o clico de entrega
    - É leve e portatil

    [] Isolamento
    - Como funciona?
        - CGroups
        - Namespace
        - Unshare
    
    [] OCI - Open Container Initiative
    - O que é?
        - Estrutura de governança
        - Visa facilitar a interoperabilidade
        - Garante padrões mantendo a flexibilidade
        - Runtime; Image; Distro
    - Objetivo
        - Promover contêineres agnósticos
        - Protabilidade
        
