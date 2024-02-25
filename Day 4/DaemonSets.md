![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/722934d4-ea57-443f-82f3-3cf3122e4c60)

```
apiVersion: apps/v1
kind: DaemonSet
metadata: 
  name: elasticsearch
  namespace: kube-system
spec:
  selector:
    matchLabels:
      env: test
  template: 
    metadata:
      name: elasticsearch
      labels:
        env: test
    spec: 
      containers: 
        - name: elasticsearch
          image: registry.k8s.io/fluentd-elasticsearch:1.20
```
