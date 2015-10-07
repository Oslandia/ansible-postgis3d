# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define "trusty" do |trusty|
    trusty.vm.box = "ubuntu/trusty64"
  end

  config.vm.define "jessie" do |jessie|
    jessie.vm.box = "debian/jessie64"
  end

  config.vm.define "sid" do |sid|
    sid.vm.box = "loicfrering/debian-unstable"
  end

  config.vm.network "public_network"
  config.vm.hostname = "postgis3d"

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "test.yml"
  end

  config.vm.provider "virtualbox" do |v|
    v.memory = 3096 # sfcgal compilation needs a minimum of 3GB
  end
end
