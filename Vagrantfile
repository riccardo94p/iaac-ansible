Vagrant.configure("2") do |config|
	# Automatically downloads CentOS image from Vagrant cloud
	config.vm.box = "centos/7"
		
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
	
	# Tell the VM we want tu run Ansible on it
	# ansible_local means that it will run Ansible inside the VM
	#config.vm.provision "ansible_local" do |ansible|
	#	ansible.playbook = "main.yaml"
	#end
end
