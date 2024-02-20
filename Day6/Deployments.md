What is Deployment?

It is above replicaset. It is also object. Deployment manages replicaset. 

Deployment maintains the replicaset version. If you create replicaset as V1 version then you done some chnges then it will create as V2. 

**If you increace PODS and then try rollout with decrease in Pod then it will have same POD as that current version. It will not reduce.**

Still replicaset will create POD. But Replicaset will be managed by Deployment. Basically it will help for version controlling of your application.

**Whenever you create new version then it will delete old replicaset and pods.**

If there is any problem with deployment then kubernetes automatically roll back to older version.

There are two strategies to rollout update:

1. Recreate : If you using imperactive command to change version of image then it will use recreate strategy. In this it will delete all pods and Replicaset , It will create new one 
2. Rolling Update :

YAML For Deployment:

apiVersion: apps/v1 

kind: Deployment

metadata:

  name: test
  
  labels:
  
    name: test
    
	type: prod
 
spec:

  template:
  
  replicas: 3
  
  metadata:
  
    name: test
    
    labels:
    
      name: test
      
	  type: prod 
   
  spec:
  
    containers:
    
      - name: nginx
      
        image: nginx
        
  selector:
  
    matchLabels:
    
       type: prod	

 ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/9b65da08-d02e-4fbe-9e55-0920fce86223)
      

To CHECK POD and Replicaset

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/80a820dd-2ea5-49af-9ad0-721e8de1b58a)

To validate Labels:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/3e726a9e-8664-4942-ad2c-1d825a85fd16)


All Commands related to Deployment

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/1fadc56b-dcf5-45c1-823b-24989e933617)


**Imperactive Command:**

**kubectl create deployment --image=nginx nginx --replicas=4 --dry-run=client -o yaml > nginx-deployment.yaml**


