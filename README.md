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

### Things to think about:
This playbook was made fairly generic to allow for customers to build upon it. A lot of our customers will do the following:
- Add a DB backup prior to doing the upgrade.
- Add silencing to their monitoring tools before turning off services, remove silencing once the upgrade is complete.
- Build a farm using scalr-ctl once the upgrade is complete to ensure basic functionality is working (automated testing): https://github.com/scalr-tutorials/Ansible-Farm-Template

