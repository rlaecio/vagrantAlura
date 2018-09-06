Vagrant.configure("2") do |config|

	# ubuntu machine
	config.vm.box = "ubuntu/trusty32"

	# web virtual machine
	config.vm.define :web do |web_config|
		web_config.vm.network :private_network, :ip => "192.168.50.10"
		web_config.vm.provision "shell", path : "manifests/bootstrap.sh"
		web_config.vm.provision "puppet" do |puppet|
			puppet.manifest_file = "web.pp"
		end
	end
end
