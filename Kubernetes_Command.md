# install microk8s in ubuntu
```
snap install microk8s --classic
```
# start microk8s
```
microk8s start
```
# add alias
```
vi .bashrc
```
```
alias kubectl='microk8s kubectl'
```
```
source .bashrc
```
# alias microk8s kubectl to kubectl
```
alias kubectl='microk8s kubectl'
```
# get namespace
```
kubectl get ns
```
# get pods linked with namespace
```
kubectl get pod -n <namespace_name>
```
# create namespace
```
kubectl create ns <namespace_name>
```
# edit namespace
```
kubectl edit ns <namespace_name>
```
# get pods
```
kubectl get pod
```
# describe pod
```
kubectl describe  pod
```
# get pod explaination
```
kubectl explain pod
```
# create Pod
```
kubectl apply -f <pod_file> -n <namespace_name>
```
If namespace is not mentioned pod will get added to default namespace
# describe pod
```
kubectl describe pod <pod_name> -n <namespace_name>
```
# edit pod
```
kubectl edit pod <pod_name> -n <namespace_name>
```
# create replicaset
```
kubectl apply -f <replicaset.yml>
```
# get replicaset
```
kubectl get replicaset
```
# edit replicaset
```
kubectl edit replicaset <replicaset_name>
```
# delete replicaset
```
kubectl delete  replicaset <replicaset_name>
```
# search previously used command
ctrl+R
# create nginx image by command
```
kubectl run nginx --image=nginx
```
# create deployment
```
kubectl apply -f deployment <deployment.yml>
```
# describe deployment
```
kubectl describe deployment <deployement_name>
```
# record
```
kubectl apply -f deployment.yml --record
```
# rollout status
```
kubectl rollout status <deployment_name>
```
# get rollout history
```
kubectl rollout history <deployement_name>
```
# edit deployment
```
kubectl edit  <deployement_name> --record
```
# update image in deployment 
```
kubectl det image <deployement_name> image_name=image_name:image_version
kubectl set image deployment.apps/nginx-deployment nginx=nginx:1.25.4.8
```
# undo/rollback deployement
```
kubectl rollout undo <deployement_name> --record
```
# copy file one step back folder
```
cp file_name ../
```
# get Persistent voulume
```
kubectl get pv
```
# get Persistent volume claim
```
kubectl get pvc
```
# get service
```
kubectl get svc
```
# get into pod
```
kubectl exec -it pod_name bash
```
# login to mysql 
```
mysql -u root -p
```

