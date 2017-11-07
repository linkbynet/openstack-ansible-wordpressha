# Ansible playbooks for deploying an highly availlable Wordpess on an openstack Cloud

Thoses playbooks will install an highly availlable Wordpress (1 LB (lbaas) + 2 Webs + 1 Sql)
This is a POC work, intended to provides somes examples on how it can be done.
If you want to use it for production, please review playbooks.


## Parameters :
* action : create|remove
* cloud : cloud config to use (See/configure vars/{env}.yml)
* wpname : wordpress deployment name (used for multi WP platforms)


## Deploy a wordpress : 
```
ansible-playbook -i hosts -e "action=create cloud=lbn-aub-01-demo wpname=bca" site.yml
```

## Delete wordpress :
```
ansible-playbook -i hosts -e "action=remove cloud=lbn-aub-01-demo wpname=bca" site.yml
```

## Credits : 
* https://github.com/ansible/ansible-examples/tree/master/wordpress-nginx_rhel7
* https://github.com/squidboylan/osops-tools-contrib/tree/master/ansible/lampstack

