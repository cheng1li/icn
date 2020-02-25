# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1804"
  config.vm.hostname = "ubuntu18"
  config.vm.synced_folder ".", "/vagrant"
  config.vm.network "private_network", type: "dhcp", libvirt__network_address: "192.168.123.0"
  config.vm.network "private_network", type: "dhcp", libvirt__network_address: "192.168.124.0"
  config.vm.provider :libvirt do |libvirt|
    libvirt.graphics_ip = '0.0.0.0'
    # add random suffix to allow running multiple jobs
    libvirt.random_hostname = 'yes'
    libvirt.cpus = 32
    libvirt.memory = 55296
    libvirt.machine_virtual_size = 400
  end
end
