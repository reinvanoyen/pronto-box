Vagrant.configure("2") do |config|

	config.vm.box = "debian/contrib-jessie64"

	config.vm.network "forwarded_port", guest: 80, host: 8080

	config.vm.synced_folder "../pronto", "/home/vagrant/pronto", create: true, owner: "www-data", group: "www-data"
	config.vm.synced_folder "../pronto-template", "/home/vagrant/pronto-template", create: true, owner: "www-data", group: "www-data"

	config.vm.provision "shell" do |s|
		s.path = "./setup.sh"
	end

end