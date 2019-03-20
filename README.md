Tasks in the Role
=========


<img width="80" height="80" src="https://cloud.google.com/_static/images/cloud/icons/favicons/onecloud/apple-icon.png" >


  - Install Google SDK and "gcloud" CLI tool. **MacOS and Debian/Redhat based distros support**
  - Deploy a K8s cluster using Google Kubernetes Services.
  - Activate RBAC into k8s Cluster



<img title="Helm" width="80" height="80" src="https://cdn-images-1.medium.com/max/1600/1*HSw4KtK66LSAP8qEPSq0nQ.png">


- Install Tiller server into k8s cluster 
- Install Helm client **MacOS and Debian/Redhat based distros support**




<img title="Istio" width="80" height="80" src="https://cdn-images-1.medium.com/max/1600/1*IygIdDiNgq3YBzTtaYvIWA.png">


- Install Istio Service Mesh




<img title="Knative" width="80" height="80" src="https://cdn-images-1.medium.com/max/1200/1*fWtVse6DItxvOBowU85Www.png">


- Install Knative and Dependencies




<img title="Kiali" width="120" height="80" src="https://cdn-images-1.medium.com/max/600/1*YishSzZFrWdMIJS4JF6LZw@2x.png">


- Install Kiali to Service Mesh Observavility



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
<br/>
<br/>

***


3. The Following permissions has been assigned to Service Account. 
    - Owner
    - Service Management Administrator
    - Service Usage Admin


<p align="center">
<img width="850" height="550" src="img/grant_roles_sa.JPG" title="Roles SA">
</p>

***

- Download the key to the local path for deploy this playbook


<p align="center">
<img width="850" height="550" src="img/create_key.JPG" title="Key SA">
</p>

***




### To Run and Test PaaS demo

```bash
ansible-playbook site.yaml -i hosts  -e gcp_keyfile=/Path/to/key.json
```

---


## Note
- Platforms like a Azure or AWS to soon.
* Windows Environment to soon.





Author Information
------------------

<img width="120" height="120" src="https://everislima.hiringroom.com/data/accounts/everislima/profile.jpg" >



__PaaS Knowledge Group__

## Members:
* Adrián González
* Alejandro Torres
* Antonio Sequera
* Iñigo Iglesias
* Jeferson Ortiz
* Jesus Sanchez
* Jonis González
* Jordy Peralta
* Miguel Rivera
* Mostafa Charem
* Omar Rodriguez
* Pedro Peñaloza
* Yasser Aquino






 