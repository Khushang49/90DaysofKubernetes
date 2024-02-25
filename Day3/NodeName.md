If you want to mention Pod craetion on specific Node you can mention nodename parameter in Pod YAML. If any scheduler is not working then we need to use this NodeName parameter.

**If you want to add port in different node then you need to delete that pod and then create pod with NodeName parameter. We cant add on existing.**

example:
```
apiVersion: v1
kind: Pod
metadata: 
  name: test
  labels:
    env: test
spec:
  containers:
    - name: test
      image: nginx
      ports:
        - containerPort: 80
  nodeName: node02 
  restartPolicy: Never
```
![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/97c9c259-8ac2-4431-9491-c2f0354ccafd)



![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/4d30c74d-647a-4714-b26c-76a641366383)


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/6e8387fe-e2a7-4da3-b302-c99e8e8fb75b)

```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  -  image: nginx
     name: nginx
  nodeName: node01
```

