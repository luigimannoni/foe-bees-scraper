# -*- mode: ruby -*-
# vi: set ft=ruby :

LOCAL_FOLDER = Dir.pwd
DOCKER_COMPOSE_CONF = "/vagrant/docker-compose.yml"

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "public_network"
  config.vm.synced_folder "#{LOCAL_FOLDER}", "/vagrant", type: "virtualbox"

  config.vm.provision :docker
  config.vm.provision :docker_compose, yml: DOCKER_COMPOSE_CONF, compose_version: '1.17.1', rebuild: true
  
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

end
