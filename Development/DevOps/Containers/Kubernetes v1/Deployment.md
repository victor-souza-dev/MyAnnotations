```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
 name: nginx-deployment
spec:
 replicas: 1
 selector:
  matchLabels:
   app: nginx-pod
 template:
  metadata:
   name: nginx-pod
  labels:
   app: nginx-pod
 spec:
  containers:
   - name: nginx-container
     image: nginx:stable
     ports:
      - containerPort: 80
```