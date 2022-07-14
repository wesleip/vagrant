# Instalação do Vagrant no POP OS 22.04

### Documentação Oficial do Vagrant: https://www.vagrantup.com/docs/installation

## Instalação do VirtualBox

~~~bash
$ sudo apt install virtualbox
~~~

## Atualização dos pacotes instalados na distribuição

~~~bash
$ sudo apt update && sudo apt upgrade -y
~~~

### Download do pacote Vagrant usando o comando curl

~~~bash
$ curl -O https://releases.hashicorp.com/vagrant/2.2.6/vagrant_2.2.6_x86_64.deb
~~~

## Instalando o pacote .deb baixado na maquina

~~~bash
$ sudo apt install ./vagrant_2.2.6_x86_64.deb
~~~

## Verificando a instalação do Vagrant na máquina

~~~bash
$ vagrant --version
~~~

## Saida desejada após a execução do comando acima

~~~bash
Vagrant 2.2.6
~~~

## Criando um diretório para o primeiro projeto com Vagrant

~~~bash
$ mkdir ~/primeiro-projeto-vagrant
$ cd ~/primeiro-projeto-vagrant
~~~
## Criando a primeira box usando o CentOS 7 como exemplo

Para criar a primeira box utilize o arquivo Vagrantfile
