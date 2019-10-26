# Docker

Lista com comandos úteis para serem utilizados no docker.

## Usando
> Verificar se pode acessar e baixar imagens do Docker Hub:
```bash
docker run hello-world
```
> Listar os comandos:
```bash
docker
```
> Opções para comando específico:
```bash
docker subcomando-docker --help
```
> Estrutura dos comandos:
```bash
docker [option] [command] [arguments]
```

## Instalação

Instalação do docker no ubuntu.

> Atualizar lista atual de pacotes:
```bash
sudo apt update
```
> Instalar alguns pacotes de pré-requisitos para instalar pacotes via HTTPS:
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
> Adicionar chave GPG para o repositório oficial do Docker:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
> Adicionar repositório do Docker às fontes do APT:
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
> Atualizar lista atual de pacotes com os pacotes Docker:
```bash
sudo apt update
```
> Certificar que o Docker irá ser instalalado a partir do repositório do Docker em vez do repositório padrão do Ubuntu:
```bash
apt-cache policy docker-ce

#Saída
#docker-ce:
  #Installed: (none)
  #Candidate: 18.03.1~ce~3-0~ubuntu
  #Version table:
     #18.03.1~ce~3-0~ubuntu 500
        #500 https://download.docker.com/linux/ubuntu bionic/stable amd64 Packages
```
> Instalar Docker
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
> Verificar se o Docker está sendo executado:
```bash
sudo systemctl status docker

#sudo /etc/init.d/docker start
```
> Verificar se o Docker está sendo executado:
```bash
sudo systemctl status docker
```
> Executar comandos Docker sem sudo:
```bash
sudo usermod -aG docker ${USER}
```
```bash
su - ${USER}
```
```bash
id -nG
```

## Instalação Docker-Compose
```bash
sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

## Fontes
[Docker Instalação](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
[Instalação](https://www.digitalocean.com/community/tutorials/como-instalar-e-usar-o-docker-no-ubuntu-18-04-pt)
