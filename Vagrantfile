Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.provision :shell, path: "src/scripts/install_docker.sh"
  
  config.vm.provision :shell, path: "src/scripts/init_postgres.sh"
  config.vm.provision :shell, path: "src/scripts/init_scylla.sh"

  # Volumes
  config.vm.synced_folder "src/volumes/postgres/", "/mnt/postgres_data"
  config.vm.synced_folder "src/volumes/scylla/", "/mnt/scylla_data"
end
