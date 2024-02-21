If you want to mention Pod craetion on specific Node you can mention nodename parameter in Pod YAML. If any scheduler is not working then we need to use this NodeName parameter.

**If you want to add port in different node then you need to delete that pod and then create pod with NodeName parameter. We cant add on existing.**

example:

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


    ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/97c9c259-8ac2-4431-9491-c2f0354ccafd)

