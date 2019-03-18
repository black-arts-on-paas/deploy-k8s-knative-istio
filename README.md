Roles Name
=========

### GCP: Install SDK Google
### Istio: Install Istio Control and Data plane
### Knative: Install Knative and Dependencies
### Helm: Install Tiller server and Helm


Requirements
------------

### GCP: Just need to add google compute engine key path to deploy this current example.


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

## Example for Google Cloud Compute
----------------

---
    - hosts: local-deploy
      connection: local
      gather_facts: yes
      vars:
        platform: gcp 
      pre_tasks:
        - import_tasks: "{{ playbook_dir }}/roles/everis-paas-demo/tasks/{{ platform }}/install_{{ platform }}_sdk.yaml"
      roles:
        - everis-paas-demo
---

## To Run and Test PaaS demo

```bash
ansible-playbook site.yaml -i hosts  -e gcp_keyfile=/Path/to/key.json
```

## Note
More Platforms like a Azure or AWS to soon. 

License
-------

BSD

Author Information
------------------

Jesus Sanchez
Jonis González

 