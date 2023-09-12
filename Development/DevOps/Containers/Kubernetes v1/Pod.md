---
aliases:
---

```
apiVersion: v1
kind: Pod
metadata:
 name: pod-2
 labels:
  app: labelPod-2
spec:
 containers:
  - name: container-1
 image: nginx:latest
 ports:
 - containerPort: 80
 env:
 - name: "MYSQL_ROOT_PASSWORD"
 value: "q1w2e3r4"
 - name: "MYSQL_DATABASE"
 value: "empresa"
 - name: "MYSQL_PASSWORD"
 value: "q1w2e3r4"
 envFrom:
  - configMapRef:
     name: sistema-configmap
```