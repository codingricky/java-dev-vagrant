# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "lucid32"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://files.vagrantup.com/lucid32.box"

  # Boot with a GUI so you can see the screen. (Default is headless)
   config.vm.boot_mode = :gui

 #Chef config
  config.vm.provision 'chef_solo' do |chef|
    chef.cookbooks_path = ['cookbooks']
    chef.add_recipe 'apt'
    chef.add_recipe 'java'
    chef.add_recipe 'git'
    chef.add_recipe 'openssh'
    chef.add_recipe 'maven'
    chef.add_recipe 'curl'
    chef.add_recipe 'wget'
  end

end
