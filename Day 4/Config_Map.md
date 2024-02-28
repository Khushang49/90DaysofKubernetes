





![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/7fbf6127-d6ce-45db-8bd4-30b1ff3e9a34)


**If you want to add all secrets then mention envFrom otherwise mention env.**

Questions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/b1acae35-738c-4339-bc15-aa5e716e68fc)
```
apiVersion: v1
kind: ConfigMap
metadata:
  name: webapp-config-map
data: 
  APP_COLOR: darkblue 
  APP_OTHER: disregard
```

```
kubectl create configmap configmapname --from-literal=key=value
```

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/a5587e4b-d959-491c-b4af-5650b72480fe)


```
apiVersion: v1
kind: Pod
metadata: 
  name: webapp-color
spec: 
  containers: 
    - name: webapp-color
      image: kodekloud/webapp-color
      env: 
        - name: APP_COLOR                 ##Parameter name in Config MAp
            valueFrom:
              configMapKeyRef:
                name: webapp-config-map   ##COnfig map name
                key: APP_COLOR            ##Parameter name in Config MAp
```
