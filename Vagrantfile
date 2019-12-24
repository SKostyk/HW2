Vagrant.configure("2") do |config|
  config.vm.define "cent1" do |cent1|
 
    cent1.vm.box = "centos/7"
    cent1.vm.network "private_network", ip: "192.168.1.10"

	
	
	
    cent1.vm.provider :virtualbox do |v|
	
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "cent1"]
    end
	
  end
  config.vm.define "cent2" do |cent2|
    cent2.vm.box = "centos/7"
    cent2.vm.network "private_network", ip: "192.168.1.11"

	
	
    cent2.vm.provider :virtualbox do |v|
	
      v.customize ["modifyvm", :id, "--natdnshostresolver2", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "cent2"]
    end
  
  end
end

