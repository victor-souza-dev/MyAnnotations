#### Kubectl | Imperative

View clusters: `kubectl get nodes
###### Pod
View pods: `kubectl get pods
View pods in real-time: `kubectl get pods --watch
View pods with network info: `kubectl get pods -o wide
View info pod: `kubectl describe pod "namePod"`
Create pod: `kubectl run "namePod" --image="image:latest" 
Edit info pod: `kubectl edit pod "namePod"`
Open SSH in pod: `kubectl exec -it "namePod" -- bash
Delete pod: `kubectl delete pods --all
###### Service
View info service: `kubectl get svc
View pods with network info: `kubectl get svc -o wide
Delete pod: `kubectl delete svc --all

###### ReplicaSet
View replicasets: `kubectl get rs

###### Deployment
View deployments: `kubectl get deployments
Historic change: `kubectl rollout history deployment nginx-deployment
Define explication for changes: `kubectl annotate deployment nginx-deployment kubernetes.io/change-cause="texto"
Rollback version: `kubectl rollout undo deployment nginx-deployment --to-revision="versionNumber"

###### Container
Access container: `kubectl exec -it "namePod" --container "nameContainer" -- bash

#### Kubectl | Declarative

###### Pod | SVC | Rs | Deployment
Create pod/service/etc: `kubectl apply -f ./pod.yaml 
Delete pod, SVC, rs, deployment: `kubectl delete -f ./pod.yaml

###### Deployment
Create deployment and register change: `kubectl apply -f ./pod.yaml --record

#Kubernetes  