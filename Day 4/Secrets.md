https://spacelift.io/blog/kubernetes-secrets

Questions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/8ad2ccc6-677b-46da-af3c-5f331dca1667)

Using YAML
```
apiVersion: v1
kind: Secret
metadata: 
  name: db-secret
stringData: 
  DB_Host: sql01
  DB_User: root
  DB_Password: password123
```

Using Imperative command:
```
kubectl create secret generic test --from-literal=DB_Host=sql01 --from-literal=DB_User=root --from-literal=DB_Password=password123
```

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/9d1287a7-4edf-4045-bdb5-75c1c7785f05)

using YAML:

```
apiVersion: v1
kind: Pod
metadata: 
  name: webapp-pod
  labels: 
    pod: secret
spec: 
  containers: 
    - name: webapp-pod
      image: kodekloud/simple-webapp-mysql
      envFrom:
        - secretRef:
            name: db-secret
```
