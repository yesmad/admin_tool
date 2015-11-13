# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "CentOS-6.5-x86_64"

  config.vm.box_url = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.5-x86_64-v20140311.box"

  config.vm.network :forwarded_port, guest: 80, host: 8000
  config.vm.network :private_network, ip: "192.168.33.40"

  # Mount the parent directory at /mnt/fuelphp
  config.vm.synced_folder "~/MyApp/Yesmad/web/admin_tool", "/vagrant/",
    :owner => "vagrant", :group => "vagrant",
    :mount_options => ["dmode=777,fmode=777"]
  # Speed up with NFS. nfsd is needed on Host OS
  #config.vm.synced_folder "../", "/mnt/fuelphp", :nfs => true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider :virtualbox do |vb|
  #   # Don't boot with headless mode
  #   vb.gui = true
  #
  #   # Use VBoxManage to customize the VM. For example to change memory:
  #   vb.customize ["modifyvm", :id, "--memory", "1024"]
  # end
  #
  # View the documentation for the provider you're using for more
  # information on available options.

  # Enable provisioning with chef solo, specifying a cookbooks path, roles
  # path, and data_bags path (all relative to this Vagrantfile), and adding
  # some recipes and/or roles.
  #
#  config.vm.provision :chef_solo do |chef|
#     chef.cookbooks_path = "./cookbooks"

#     chef.add_recipe "iptables"
#chef.add_recipe "mysql::server"
#      chef.add_recipe "mysql56"


     # remi
#     chef.add_recipe "yum-remi"
#     chef.add_recipe "php55-remi"
     #chef.add_recipe "php56-remi"
#     chef.add_recipe "phpmyadmin-remi"

     # ius
     #chef.add_recipe "yum::ius"
     #chef.add_recipe "php55-ius"
     #chef.add_recipe "php54-ius"
     #chef.add_recipe "phpmyadmin"

 #    chef.add_recipe "git"
     #chef.add_recipe "beanstalkd"

 #    chef.add_recipe "phpunit"
 #    chef.add_recipe "fuelphp"

     #chef.add_recipe "mongodb"
     #chef.add_recipe "redis"
     #chef.add_recipe "yum-update"

  #   # You may also specify custom JSON attributes:
#     chef.json = {
#        "yum" => {
#            "remi-repo" => "remi-php55",
#            #"remi-repo" => "remi-php56",
#            "ius_release" => "1.0-13"
#        },
#        "php" => {
#            "date.timezone" => "Asia/Tokyo"
#        },
#        "mysql" => {
#          "password" => ''
#        },
##"mysql" => {
##           "server_root_password"   => "root",
##           'server_debian_password' => "root",
##           'server_repl_password'   => "root",
##           "allow_remote_root"      => true, # allows us to connect from the host
##           "bind_address"           => "0.0.0.0",
##         },
#         # which databases should we make?
#         "db" => [
#           "fuel_test",
#           "fuel_dev"
#         ],
#      }
#  end
end

