Vagrant.configure(2) do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.provider :virtualbox do |v| v.customize ["modifyvm", :id, "--memory", 2048]
    end
    config.vm.define "vmMain" do |vmMain|
        vmMain.vm.hostname = "vmMain"
        vmMain.vm.network :"private_network", ip: "192.168.3.2"
    end
  
    config.vm.define "vmAgent1" do |vmAgent1|
        vmAgent1.vm.hostname = "vmAgent1"
        vmAgent1.vm.network :"private_network", ip: "192.168.3.3"
    end
  
    config.vm.define "vmAgent2" do |vmAgent2|
        vmAgent2.vm.hostname = "vmAgent2"
        vmAgent2.vm.network :"private_network", ip: "192.168.3.4"
   end
end