#Data de criação: 13.07.2022
#Versão: 0.01
#Testado e homologado no Linux POP OS 22.04
#Arquivo de configuração Vagrantfile para webserver Apache HTTP Server

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 config.vm.define "webserver" do |web|
  #Configuração do nome do BOX Local do Vagrant
  config.vm.box = "centos/7"
  #Link de download da Imagem do  Oficial
  web.vm.box_url = "https://app.vagrantup.com/centos/boxes/7/versions/2004.01/providers/virtualbox.box"
  #Configuração do Hostname do BOX no Vagrant
  web.vm.hostname = "webserver"
  #Configuração do Endereçamento Público IPv4 do BOX do Vagrant
  #OBSERVAÇÃO: Utilizar as configurações de acordo com a sua Interface de Rede
  web.vm.network "public_network", ip: "10.17.0.100", bridge: "wlp2s0"
  #Configuração da Máquina Virtual do BOX no VirtualBOX do Vagrant
  web.vm.provider "virtualbox" do |vb|
   #Configuração do nome da Máquina Virtual no VirtualBOX do Vagrant
   vb.name = "centos_7"
   #Configuração da quantidade de Memória RAM da Máquina Virtual no VirtualBOX do Vagrant
   vb.memory = "1024"
   #Configuração da quantidade de vCPU's da Máquina Virtual no VirtualBOX do Vagrant
   vb.cpus = "2"
   #Fim do Bloco de Configuração: Provider (virtualbox |vb|)
  end
   #Aqui começa a configuração dos serviços necessários para que o servidor funcione
  config.vm.provision "shell", inline: <<-SHELL
  sudo su
  #Instalação do pacote httpd
  yum install httpd -y
  #Após a instalção o comando abaixo inicia o serviço httpd
  systemctl start httpd
  #O comando abaixo torna o serviço httpd inicializável automaticamento toda vez que o servidor iniciar
  systemctl enable httpd
SHELL
 end
end
