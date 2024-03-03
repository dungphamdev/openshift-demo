# openshift-demo

this repo is for learning OpenShift, k8s purpose

- bubble-animation: follow this tutorial: https://www.youtube.com/watch?v=pOGMSOotSn0

- lab01-helloworld-pipeline: set up a simple pipeline with tekton

- lab02-deploy-with-argocd: set up an application with argoCD
TODO: change the hello world text to with a name from environment and pass the value to the name from CD pipeline

some useful commands:
Command # 1 --------- 
- Add cluster role to user 
- oc adm policy add-cluster-role-to-user cluster-admin -z openshift-gitops-argocd-application-controller -n openshift-gitops 

Command # 2 --------- 
- Get Argo password 
- argoPass=$(oc get secret/openshift-gitops-cluster -n openshift-gitops -o jsonpath='{.data.admin\.password}' | base64 -d)
- echo $argoPass 
