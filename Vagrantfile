# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.name "test01"
  config.vm.box = "user/image"
  config.vm.network "private_network", ip: "192.168.1.XX"
  config.vm.synced_folder '.', '/vagrant', disabled: true #vagrant tries to mount SMB shares by default https://www.vagrantup.com/docs/synced-folders/ you can configure a different directory and credentials or leave it disabled to just bring up the VM
  config.vm.provision "bootstrap", type: "shell", run: "never" do |s| #To further limit provisioning that is ran, edit if you would like pacakges installed, etc.
    s.inline = "echo hello"
  end
  config.vm.provider "hyperv" do |hv|
    hv.vmname = "test01"
    hv.memory = "1024"
    hv.cpus = "2"
  end
  config.ssh.username = "vagrant"
  config.ssh.private_key_path = "C:/Users/$USERNAME$/.ssh/id_rsa" #With "ssh-keygen.exe -t rsa -m PEM" used to generate ssh key for user, set up using ssh-keygen.exe and ssh.exe from https://github.com/PowerShell/Win32-OpenSSH/releases/tag/v7.9.0.0p1-Beta placed in C:\Program Files\OpenSSH and '$Env:path += ";c:\Program Files\OpenSSH"' invoked before "vagrant up" execution.
end
