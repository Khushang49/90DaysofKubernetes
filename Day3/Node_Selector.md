**Node Selector is only used when you want to create Pods in specific Node.** At that time we need to use Node selector. But for this you need to first label the node. Then only you can use node selector.

Before that you need to label the node. 

To Check available nodes

**#kubectl get nodes**

To label Nodes

**#kubectl label node node01 env=test**

Syntax: **kubectl label node nodename keylabel=valuelabel (no space)**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/a5e17055-6744-4d01-8e2f-1e2a5efd893b)

Now mention this label in Yaml in **nodeSelector**.


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e2044de2-2c8f-4247-b5ef-370087de24cc)


Syntax

apiVersion: v1

kind: Pod

metadata: 

  name: testpod
  
  labels:
  
    name: test
    
    env: prod

spec:

  containers:
  
    - name: testcontainers
    
      image: nginx
    
    nodeSelector:
    
      env: test
      
