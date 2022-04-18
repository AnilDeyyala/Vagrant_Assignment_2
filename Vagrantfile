# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "apache" do |apache|
    apache.vm.box = "ubuntu/trusty64"
    apache.vm.network "private_network", ip: "192.168.33.20"
    config.vm.synced_folder "C:/Users/anil.deyyala/projects/multiVMs", "/vagrant_data"
    apache.vm.provider "virtualbox" do |vb|
        vb.memory = 1048
        vb.cpus = 2
    end
  end

  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/trusty64"
    db.vm.network "private_network", ip: "192.168.33.30"
    config.vm.synced_folder "C:/Users/anil.deyyala/projects/multiVMs", "/vagrant_data"
    db.vm.provider "virtualbox" do |vb|
        vb.memory = 2048
        vb.cpus = 1
    end
  end
end
