# Ansible

More information about deployment is in our wiki.

Use a command like this to run this playbook.  If you've satisfied all the prerequisites then it should install
Ruby, SOLR and configure most things in the application to work with the wacky configuration that Jim has set up.

```
ansible-playbook site.yml -i staging
```

## General info

*Playbooks* contain *plays* contain *tasks* use *modules*.

This is a helpful overview: https://www.ansible.com/resources/videos/quick-start-video

## Examples

- This will do a ping (module) directly: `ansible web -i staging -m ping`
- Run playbook on environment: `ansible-playbook site.yml -i staging`
- List remote directory: `ansible web -i staging -a "ls"`
- Show working directory: `ansible web -i staging -a "pwd"`
- Run playbook: `ansible-playbook site.yml -i staging`
- Get role from ansible galaxy: `ansible-galaxy install geerlingguy.ruby`
- Get role from galaxy to your roles directory: `ansible-galaxy install --roles-path ./roles geerlingguy.ruby`


