ENV["LC_ALL"] = "en_US.UTF-8"
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["setextradata", :id, "VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled", 0]
    vb.memory = 1024
    vb.cpus = 1
    vb.customize [
      "modifyvm", :id,
      "--hwvirtex", "on",
      "--nestedpaging", "on",
      "--largepages", "on",
      "--ioapic", "on",
      "--pae", "on",
      "--paravirtprovider", "kvm",
    ]
  end

  config.vm.provision "shell", :inline => 'sudo yum install -y  yum -y install yum-plugin-fastestmirror'
  config.vm.provision "shell", :inline => 'sudo yum groupinstall -y "Development Tools"'

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

  config.vm.define :node05 do |node|
    node.vm.hostname = "node05"
    node.vm.network :private_network, ip: "192.168.11.15"
  end

end
