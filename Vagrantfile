# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  # Set box configuration
  config.vm.box = "dev_box"
  config.vm.box_url = "http://files.vagrantup.com/lucid32.box"
  config.vm.host_name = "ubuntu.dev"
  # Assign this VM to a host-only network IP, allowing you to access it via the IP.
  config.vm.network :hostonly, "192.168.56.2"
  
  config.vm.share_folder "v-devdata", "/DevDisk", "/Volumes/DevDisk/"

  # Enable provisioning with chef solo, specifying a cookbooks path (relative
  # to this Vagrantfile), and adding some recipes and/or roles.
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "cookbooks"
    chef.data_bags_path = "data_bags"
    chef.add_recipe "vagrant_main"

    chef.json.merge!({
      "mysql" => {
        "server_root_password" => "root",
        "server_repl_password" => "root",
        "server_debian_password" => "root",
        "bind_address" => "127.0.0.1"
      }
    })
  end
end
