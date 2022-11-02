Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.name = "desafio04"
  end
  #config.vm.box = "ubuntu/trusty64"
  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "public_network"
  config.vm.synced_folder "./nginxdocker", "/home/vagrant"
  
  config.vm.provision "shell", inline: <<-SHELL
     sudo apt update
     sudo apt install docker.io -y
     sudo docker build -t nginx-desafio04 .
     sudo docker run --name nginx -p 80:80 -d nginx-desafio04
     
  SHELL
end
