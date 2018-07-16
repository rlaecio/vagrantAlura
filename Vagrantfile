Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.provider "virtualbox" do |v|
	   v.memory = 1024
  end

  config.vm.define :web do |web_config|
     web_config.vm.network "private_network", ip: "172.16.20.10"
  end
end
