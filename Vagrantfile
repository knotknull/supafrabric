# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.define "node1" do |node1|
    node1.vm.box = "centos/7"
    node1.vm.box_version = "1803.01"
    node1.vm.hostname = "node1"
    node1.vm.network "private_network", ip: "192.168.33.10"
    node1.vm.synced_folder "share/node1", "/vagrant/share"
  end

  config.vm.define "node2" do |node2|
    node2.vm.box = "centos/7"
    node2.vm.box_version = "1803.01"
    node2.vm.hostname = "node2"
    node2.vm.network "private_network", ip: "192.168.33.20"
    node2.vm.network "forwarded_port", guest: 80, host: 8080
    node2.vm.synced_folder "share/node2", "/vagrant/share"
  end

  config.vm.define "node3" do |node3|
    node3.vm.box = "centos/7"
    node3.vm.box_version = "1803.01"
    node3.vm.hostname = "node3"
    node3.vm.network "private_network", ip: "192.168.33.30"
    node3.vm.synced_folder "share/node3", "/vagrant/share"
  end

  config.vm.define "ububox" do |ububox|
    ububox.vm.box = "ubuntu/xenial64"
    ububox.vm.hostname = "ububox"
    ububox.vm.network "private_network", ip: "192.168.33.30"
    ububox.vm.synced_folder "share/ububox", "/vagrant/share"
  end
  
  
end

