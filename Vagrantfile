ENV["LC_ALL"] = "en_US.UTF-8"
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.define :node01 do |node|
    node.vm.hostname = "node01"
    node.vm.network :private_network, ip: "192.168.11.11"
  end

  config.vm.define :node02 do |node|
    node.vm.hostname = "node02"
    node.vm.network :private_network, ip: "192.168.11.12"
  end

  config.vm.define :node03 do |node|
    node.vm.hostname = "node03"
    node.vm.network :private_network, ip: "192.168.11.13"
  end

  config.vm.define :node04 do |node|
    node.vm.hostname = "node04"
    node.vm.network :private_network, ip: "192.168.11.14"
  end

end
