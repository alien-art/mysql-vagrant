# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'bento/ubuntu-16.04'
  #config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  #config.vm.network :forwarded_port, guest: 3306, host: 3306
  config.vm.provision :shell, :path => "install.sh"
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=666"]
  #config.vm.network "private_network", ip: "33.33.33.10", type: "dhcp", auto_config: false
  #config.vm.network "public_network", use_dhcp_assigned_default_route: true
  config.vm.network "public_network", ip: "192.168.1.170"
end
