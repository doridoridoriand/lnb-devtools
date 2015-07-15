# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.hostname = "vagrant"
  config.vm.box_url = "./box.json"
  config.vm.box = "lnb"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "public_network"
  config.vm.synced_folder "./dev", "/home/vagrant/dev"
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 4
    vb.memory = 4096
  end
end
