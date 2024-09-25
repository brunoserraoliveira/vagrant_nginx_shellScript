Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |vb|
    vb.name = "primeiraMaquina"
    vb.memory = 2048
    vb.cpus = 2
  end
  
  config.vm.box = "hashicorp/bionic64"
   config.vm.network "forwarded_port", guest: 80, host: 8000
   config.vm.network "public_network", ip: "192.168.1.111"

    config.vm.provision "shell", path: "script.sh"
    config.vm.synced_folder "site/" , "/var/www/html"
  config.vm.box_version = "1.0.282"
end
