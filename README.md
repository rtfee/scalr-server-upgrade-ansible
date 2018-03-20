# scalr-server-upgrade-ansible

This playbook was created for CentOS, please adjust to your Linux distribution

### Prerequisites:
- Scalr Installed
- Ansible
- Ansible hosts file:
```
[scalr-all]
scalr.db.com
scalr.app.com
scalr.worker.com

[db]
scalr.db.com

[app]
scalr.app.com

[worker]
scalr.worker.com
```

### How to run this playbook:
```
ansible-playbook upgrade.yml
```
Upgrade.yml will include scalr-server-stop.yml, scalr-yum-update.yml, and scalr-reconfig.yml
