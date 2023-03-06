Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2204"
  config.vm.box_download_options = {"limit-rate": "10240K"}
  config.vm.hostname = "jammy"
  config.vm.provision "ansible", playbook: "ansible-redmine.yml"#, tags: ["doit"]
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
end
