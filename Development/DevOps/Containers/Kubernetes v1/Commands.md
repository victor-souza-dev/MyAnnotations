#### Imperative

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
#### Declarative

###### Pod
Create pod/service/etc: `kubectl apply -f ./pod.yaml 
Delete pod: `kubectl delete -f ./pod.yaml