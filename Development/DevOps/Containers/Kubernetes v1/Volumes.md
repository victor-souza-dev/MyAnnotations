#### Hostpath

```
apiVersion: v1
kind: Pod
metadata:
 name: volume-pod
spec:
 containers:
  - name: nginx-container
    image: nginx:latest
    volumeMounts:
     - mountPath: /volume
       name: volume-pod
 volumes:
  - name: volume-pod
    hostPath:
     path: /home/volume
     type: DirectoryOrCreate
```

#### gcePersistentDisk (Google Cloud Engine Persistence Disk)

Volume storage in configured the Google Cloud:

###### PV (Persistent Volume)

```yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: pv-1
spec:
  capacity:
    storage: 400Gi
  accessModes:
  - ReadWriteOnce | ReadWriteMany | ReadOnlyMany | ReadOnlyOnce
  gcePersistentDisk:
    pdName: my-data-disk
```

###### PVC (Persistent Volume Claim)

```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvc-1
spec:
  accessModes:
  - ReadWriteOnce | ReadWriteMany | ReadOnlyMany | ReadOnlyOnce
  resources:
    requests: 
	 storage: 10Gi
  storageClassName: standard
```

###### Access PV

```yaml
apiVersion: v1
kind: Pod
metadata:
 name: pod-pv
spec:
 containers:
  - name: nginx:latest
    image: nginx:latest
    volumeMounts:
     - mountPath: /volume
       name: primary-pv
	volumes:
	 - name: primary-pv
	   persistentVolumeClaim:
	    claimName: pvc-1
```


#### SC (Storage Class)

```

```