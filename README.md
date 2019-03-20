Roles
=========


<img width="80" height="80" src="https://cloud.google.com/_static/images/cloud/icons/favicons/onecloud/apple-icon.png" >


  -  Install SDK Google and "gcloud" CLI tool. **MacOS and Debian/Redhat based distros support**




<img title="Helm" width="80" height="80" src="https://cdn-images-1.medium.com/max/1600/1*HSw4KtK66LSAP8qEPSq0nQ.png">


- Install Tiller server and Helm client **MacOS and Debian/Redhat based distros support**




<img title="Istio" width="80" height="80" src="https://cdn-images-1.medium.com/max/1600/1*IygIdDiNgq3YBzTtaYvIWA.png">


- Install Istio Control and Data plane




<img title="Knative" width="80" height="80" src="https://cdn-images-1.medium.com/max/1200/1*fWtVse6DItxvOBowU85Www.png">


- Install Knative and Dependencies


Requirements
------------

### GCP: 

1. Create a Service Account for access to your GCP Project: https://console.cloud.google.com/iam-admin/serviceaccounts/project?project=youproject
<p align="center">
<img width="850" height="550" src="img/create_sa.JPG" title="Create SA">
</p>

***


2. Grant access to others accounts to use this Service Account. **Optional**
<p align="center">
<img width="850" height="550" src="img/access_sa.JPG" title="Access SA">
</p>

***


3. The Following permissions has been assigned to Service Account. 
    - Owner
    - Service Management Administrator
    - Service Usage Admin

<p align="center">
<img width="850" height="550" src="img/grant_roles_sa.JPG" title="Roles SA">
</p>


- Download the key to the local path for deploy this playbook
***
<p align="center">
<img width="850" height="550" src="img/create_key.JPG" title="Key SA">
</p>


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
Windows Environment to soon.

License
-------

BSD

Author Information
------------------


<img width="80" height="80" src="https://everislima.hiringroom.com/data/accounts/everislima/profile.jpg" >
- Digital Architecture
  - Grupo de Conociemiento Paas




 