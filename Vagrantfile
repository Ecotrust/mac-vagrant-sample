# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
 
  config.vm.box = "perk/ubuntu-2204-arm64" 
  
  config.vm.network "forwarded_port", guest: 80, host: 8080 
  config.vm.network "forwarded_port", id: "ssh", guest: 22, host: 1234
  config.vm.network "forwarded_port", guest: 8000, host: 8000


  config.vm.synced_folder "./", "/usr/local/apps",
    type: "smb",
    smb_host: "192.168.86.87"

  config.vm.provider "qemu" do |qe|
    qe.memory = "1024"
  end

end
