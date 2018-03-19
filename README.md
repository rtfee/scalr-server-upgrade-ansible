# scalr-server-upgrade-ansible

This playbook was created for CentOS, please adjust to your Linux distribution

### How to run this playbook:
```
ansible-playbook upgrade.yml
```

Upgrade.yml will include scalr-server-stop.yml, scalr-yum-update.yml, and scalr-reconfig.yml
