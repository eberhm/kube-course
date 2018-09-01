# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = "aspyatkin/ubuntu-16.04-server-amd64"
    master.vm.network "private_network", ip: "192.168.33.10"
    master.vm.synced_folder "resources/", "/resources"
  end

  config.vm.define "minion" do |minion|
    minion.vm.box = "aspyatkin/ubuntu-16.04-server-amd64"
    minion.vm.network "private_network", ip: "192.168.33.20"
    minion.vm.synced_folder "resources/", "/resources"
  end
end
