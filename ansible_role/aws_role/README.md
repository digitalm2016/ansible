Ansible Role 
=============

pip install boto3

ansible-galaxy collection install amazon.aws


Setup Vault
=============

1. Create a password for vault
   openssl rand -base64 2048 > vault.pass
   
2. Add your AWS credentials using the below vault command
   ansible-vault create group_vars/all/pass.yml --vault-password-file vault.password

   to edit this file
   ansible-vault create group_vars/all/pass.yml --vault-password-file vault.password

 
Run Playbook using vault 
=========================
 
ansible-playbook playbook.yaml --vault-password-file vault.password
