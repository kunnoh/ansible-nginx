# Ansible nginx-webserver

## Install ansible
Install using `pip` a python package manager.
```sh
python -m pip install --user ansible
```

Verify installation.
```sh
ansible --version
```


## Run ansible

Clone the code.
```sh
git clone https://'<username>'@bitbucket.org/warilo/ansible-webserver.git
```

Move to `ansible-webserver` directory.


**Set variables**

On `ansible.cfg` file,  
set location for your ssh key:  
`private_key_file=`  
set the inventory name, which is `host` file:  
`inventory=`

On `host` file, 
set your server ip:  
`ansible_host=`  
set server user:  
`ansible_user=`.

Run this command. Add `domain_name` and `email`. domain_name can be subdomain too. Email is to be used when generating certificates on let'sencrypt.

Command:
```sh
ansible-playbook deploy-nginx.yml --extra-vars "domain_name=example.com email=your-email@example.com"
```


## References
1. [Ansible docs](https://docs.ansible.com/ansible-core/2.17/getting_started/index.html)