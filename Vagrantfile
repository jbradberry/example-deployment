# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "test" do |test|
    test.vm.box = "hashicorp/bionic64"
    test.vm.network "private_network", ip: "192.168.33.10"
  end

  config.vm.define "balancer", autostart: false do |balancer|
    test.vm.box = "hashicorp/bionic64"
    test.vm.network "private_network", ip: "192.168.33.11"
  end

  config.vm.define "web", autostart: false do |web|
    test.vm.box = "hashicorp/bionic64"
    test.vm.network "private_network", ip: "192.168.33.12"
  end

end
