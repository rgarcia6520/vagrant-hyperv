# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.name "test01"
  config.vm.box = "ryan/centos7"
  config.vm.network "public_network", bridge: "Microsoft Network Adapter Multiplexor Driver"
  config.vm.provider "hyperv" do |hv|
    hv.vmname = "test01"
    hv.memory = "1024"
    hv.cpus = "1"
  end
end
