# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise64"
  config.vm.network :forwarded_port, guest: 4000, host: 4000
  config.vm.provision :shell, :path => "bootstrap.sh"
  config.vm.provision :shell, :inline => "cd /vagrant && jekyll serve --watch --force-polling", run: "always"
  config.ssh.forward_agent = true
end
