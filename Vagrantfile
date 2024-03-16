# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  if Vagrant.has_plugin? "vagrant-vbguest"
    config.vbguest.no_install  = true
    config.vbguest.auto_update = false
    config.vbguest.no_remote   = true
  end

  config.vm.define :servidorUbuntu do |servidorUbuntu|
      servidorUbuntu.vm.box = "bento/ubuntu-22.04"
      servidorUbuntu.vm.network :private_network, ip: "192.168.100.3"
      servidorUbuntu.vm.hostname = "servidorUbuntu"
      servidorUbuntu.vm.synced_folder "./sharedFolder", "/home/vagrant/sharedFolder"
      servidorUbuntu.vm.boot_timeout = 600
      servidorUbuntu.vm.provider "virtualbox" do |v|
          v.cpus = 2
          v.memory = 3072
      end
    end
  end
  