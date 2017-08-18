# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.define "lb1" do |lb1|
    lb1.vm.hostname = "lb1"
    lb1.vm.box = "lb1"
    lb1.vm.network "private_network", ip: "10.0.0.10"
    lb1.vm.provision "shell", path: "provision.sh"
  end

  config.vm.define "web1" do |web1|
    web1.vm.hostname = "web1"
    web1.vm.box = "web1"
    web1.vm.network "private_network", ip: "10.0.0.11"
    web1.vm.provision "shell", path: "provision.sh"
  end

  config.vm.define "web2" do |web2|
    web2.vm.hostname = "web2"
    web2.vm.box = "web2"
    web2.vm.network "private_network", ip: "10.0.0.12"
    web2.vm.provision "shell", path: "provision.sh"
  end
end



