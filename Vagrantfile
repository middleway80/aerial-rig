# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrant is used to isolate commits using my private github account from my professional account
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y git python-software-properties
     add-apt-repository -y ppa:git-core/ppa
     apt-get update
     curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | bash
     apt-get install git-lfs
SHELL
end
