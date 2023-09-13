```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
 name: portal-noticias-replicaset
spec:
 replicas: 1
 selector:
  matchLabels:
   app: portal-noticias
 template:
  metadata:
   name: portal-noticias
   labels:
    app: portal-noticias
  spec:
   containers:
    - name: aluracursos
      image: aluracursos/portal-noticias:1
      ports:
       - containerPort: 80
      envFrom:
       - configMapRef:
          name: portal-configmap
```