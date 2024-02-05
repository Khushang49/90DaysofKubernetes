What is Label and selectors ??

Label key value pair with no. We use label as tags. 

How to mention in YAML.

**apiVersion**: v1

**kind**: **P**od

**metadata**:

  name: test
  
  **labels**:
  
    name: test1
    
    env: prod
    
**spec**:

  **containers**:
  
    - name: test
    
      image: nginx
      



![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/03572564-810b-404c-b519-292c884d94e2)


How to check labels on pods?

**#kubectl get pods --show-labels**

Syntax of command: **kubectl get pods --show-labels**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/10b434ea-d2e7-4570-bfd6-6c0ae13d37e2)

There are two type of method to mention labels.

1. Declarative  ( mention in YAML)

2. Imperactive  (While running command)

How to add labels to existing POD?

Create pod first without labels.

**#kubectl create test2 --image nginx**

Syntax of command: **kubectl create podname --image imagename**

**#kubectl label pods test2 env=prod**

Syntax of command: **kubectl label pods podname labelkey=labelvalue**

**#kubectl get pods --show-labels**

Syntax of command: **kubectl get pods --show-labels**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/59dfc517-7b9c-4440-ad0a-54981fe99876)

How to find Pods with the help of labels?

**#kubectl get pods -l tier=prod**

Syntax of command: **kubectl get pods -l (l flag = labels) labelkey=labelvalue**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/6b8d8297-ca34-4a13-bf20-11dbd77a3212)

How to find pods who is not having specific labels?

**#kubectl get pods -l tier!=prod**

Syntax of command: **kubectl get pods -l (l flag = labels) labelkey!=labelvalue**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/3a1b4461-4bdf-4616-98b2-82c61cc58e96)

How to delete Pods with labels?

**#kubectl delete pods -l tier=prod**

Syntax of command: **kubectl delete pods -l (l flag = labels) labelkey=labelvalue**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/c086baf9-1672-4b76-ba18-13197f9de23e)



How to go Set based labels ?

There is type in which you mentioned multiple tags for matching. In this we use **in**, **notin**, **exists**.

**#kubectl get pods -l 'env in (test,prod)'**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2e9f3fbd-70d1-4d04-a413-dc9032d28cc7)

**#kubectl get pods -l ' env notin (prod,test)'**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/d95295ce-e561-4a3a-8793-0ed9de228e5a)




