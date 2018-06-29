Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"
  config.vm.provision "ansible", run: "always", type: :ansible_local do |ansible|
    ansible.galaxy_role_file = 'requirements.yml'
    ansible.playbook = "vagrant.yml"
    ansible.verbose = true
    ansible.vault_password_file = "secret"
  end
end
