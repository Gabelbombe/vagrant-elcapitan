# -*- mode: ruby -*-
# vi: set ft=ruby :

# Specify Vagrant version and Vagrant API version
Vagrant.require_version ">= 1.6.0"
Vagrant.configure(2) do | config |
  config.vm.box = "jhcook/osx-elcapitan-10.11"

  config.vm.network :private_network,
    ip: "192.168.50.4"

  config.vm.provider "virtualbox" do | vb |
    vb.gui = true
  end

  config.vm.synced_folder ".", "/vagrant", :nfs => {
    :mount_options => ["dmode=777","fmode=777"]
  }

  config.vm.provision :shell, inline: 'echo \'alias ll\''
end
