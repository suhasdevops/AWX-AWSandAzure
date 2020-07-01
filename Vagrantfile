#suhasdevops:)
#
Vagrant.configure("2") do |config|

  config.vm.box = "scorputty/centos-awx"

  config.vm.network "private_network", ip: "192.168.31.10"

  config.vm.provider "virtualbox" do |v|
		v.memory = 4096
		v.cpus = 4
	end
  
  config.vm.provision "shell", inline: <<-SHELL
     yum update
     hostnamectl set-hostname suhas-awx-tower
   SHELL
end
