# ArgoCD_start_up
walkthrough Argocd


### This demo is a walkthrough of the process of installing and accessing ArgoCD.

#### Here are some noteworthy steps:

- Use the official ArgoCD install page :https://argoproj.github.io/argo-cd/getting_started/#1-install-argo-cd
The YAML manifest for the NodePort service can be found under the argocd-server-nodeport.yaml file in the course repository
- Access the ArgoCD UI by going to https://192.168.50.4:30008 or http://192.168.50.4:30007
When accessing the ArgoCD UI, a browser SSL warning is encountered. This is happening because the ArgoCD server is not setup with SSL certificates to authenticate the server. Hence, an insecure connection is established with the server. As a result, the warning prompt is encountered and you should just bypass the warning page
Login credentials can be retrieved using : "kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d"
- Repo url: https://github.com/davincizhao/helm_cm
#### Application Deployment
A step by step guide on how to deploy an application using ArgoCD.



Python-manifests folder contains the YAML configuration for the Python hello-world application
argocd-python manifest for the Application CRD to used to deploy the Python hello-world application
