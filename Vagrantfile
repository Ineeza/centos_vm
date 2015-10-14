# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "centos-7.0-x86_64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://github.com/tommy-muehle/puppet-vagrant-boxes/releases/download/1.1.0/centos-7.0-x86_64.box"
  config.vm.define "cent7" do |cent|
    cent.vm.network :private_network, ip: "33.33.33.100"
    cent.vm.network :forwarded_port, host: 8888, guest: 80
  end
  
  # Enable provision with ansible
  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
  end

end
