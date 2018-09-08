# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", 2048]
    v.customize ["modifyvm", :id, "--cpus", 2]
  end

  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/xenial64"
    master.vm.network "private_network", ip: "172.42.42.10", netmask: "255.255.255.0"
    master.vm.hostname = "master"
    master.vm.synced_folder "resources/", "/resources"
  end

  config.vm.define "minion" do |minion|
    minion.vm.box = "ubuntu/xenial64"
    minion.vm.network "private_network", ip: "172.42.42.11", netmask: "255.255.255.0"
    minion.vm.hostname = "minion1"
    minion.vm.synced_folder "resources/", "/resources"
  end
end
