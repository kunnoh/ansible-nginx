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


## Download ansible script

Clone the code. 

```sh
git clone https://github.com/kunnoh/ansible-nginx.git
```


### Set variables
Go to `ansible-webserver` directory. 

On `ansible.cfg` file,  
set location for your ssh key, 
set the inventory name i.e `host` file:  

```sh
inventory=
private_key_file=
```

On `host` file,

set your server ip and server user:

```sh
ansible_host=
ansible_user=
```


## Run ansible

Run command below, and add `domain_name` and `email`. 
Domain_name can be subdomain too. 
Email is to be used when generating certificates on let'sencrypt. 

Command:

```sh
ansible-playbook deploy-nginx.yml --extra-vars "domain_name=example.com email=your-email@example.com"
```


## Conclusion
This will install nginx, certbot and configure nginx and add ssl to domain provided.


## References
1. [Ansible docs](https://docs.ansible.com/ansible-core/2.17/getting_started/index.html)
2. [Nginx docs](https://nginx.org/en/docs/)
3. [Certbot](https://eff-certbot.readthedocs.io/en/latest/)
