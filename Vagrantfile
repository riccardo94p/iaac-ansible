# Install vagrant-disksize to allow resizing the vagrant box disk.
unless Vagrant.has_plugin?("vagrant-disksize")
    raise "vagrant-disksize plugin is missing. Please install it using 'vagrant plugin install vagrant-disksize' and rerun 'vagrant up'"
end

# Install vagrant-hostsupdater
unless Vagrant.has_plugin?("vagrant-hostsupdater")
    raise "vagrant-hostsupdater plugin is missing. Please install it using 'vagrant plugin install vagrant-hostsupdater' and rerun 'vagrant up'"
end

Vagrant.configure("2") do |config|
	# Automatically downloads CentOS image from Vagrant cloud
	config.vm.box = "centos/7"
	config.disksize.size = "50GB"
		
	config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
		vb.cpus = "2"
	end
	
	config.vm.define "vm1" do |vm1|
		vm1.vm.hostname = "vm1.example.com"
		vm1.vm.network "private_network", ip: "192.168.33.10"
	end
	
	config.vm.define "vm2" do |vm2|
		vm2.vm.hostname = "vm2.example.com"
		vm2.vm.network "private_network", ip: "192.168.33.11"
	end
end
