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

- Create a Service Account and Service Account Key for access to your GCP Project: https://console.cloud.google.com/iam-admin/serviceaccounts/project?project=youproject



<p align="center">
<img width="700" height="400" src="img/create_sa.jpg" title="Create SA">
</p>

***

<p align="center">
<img width="700" height="400" src="img/access_sa.jpg" title="Create SA">
</p>

***

<p align="center">
<img width="700" height="400" src="img/grant_roles_sa.jpg" title="Create SA">
</p>

***
<p align="center">
<img width="700" height="400" src="img/create_key.jpg" title="Create SA">
</p>



- Download the key to the local path for deploy this pllaybook


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



- Grupo de Conociemiento Paas


 