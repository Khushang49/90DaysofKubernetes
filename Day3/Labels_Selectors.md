What is Label and selectors ??

Label key value pair with no. We use label as tags. 

How to mention in YAML.

api**V**ersion: v1

kind: **P**od

metadata:

  name: test
  
  **labels**:
  
    name: test1
    
    env: prod
    
spec:

  **containers**:
  
    - name: test
    
      image: nginx
      



![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/03572564-810b-404c-b519-292c884d94e2)


How to check labels on pods?

**#kubectl get pods --show-labels**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/10b434ea-d2e7-4570-bfd6-6c0ae13d37e2)

There are two type of method to mention labels.

1. Declarative  ( mention in YAML)

2. Imperactive  (While running command)

How to add labels to existing POD?

Create pod first without labels.

**#kubectl create test2 --image nginx**

**#kubectl label pods test2 env=prod**

**#kubectl get pods --show-labels**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/59dfc517-7b9c-4440-ad0a-54981fe99876)

