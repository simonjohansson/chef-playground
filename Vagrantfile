Vagrant::Config.run do |config|
  config.vm.box = "base64"
  config.vm.box_url = "http://files.vagrantup.com/lucid64.box"
  config.vm.define :chef_server do |chef_server|
    chef_server.vm.provision :chef_solo do |chef|
      chef.cookbooks_path = ["cookbooks"]
      chef.roles_path = "roles"
      chef.add_role("chef_server")
    end
    chef_server.vm.network(:hostonly, "33.33.33.2")
  end
end
