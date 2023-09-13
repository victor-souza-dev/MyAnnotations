
```yaml
apiVersion: v1
kind: Service
metadata:
name: svc-pod1
spec:
 type: NodePort | ClusterIP
 ports:
 - port: 80
  targetPort: 80 (default)
  nodePort: 30000
 selector:
  app: pod1
```

#Kubernetes 