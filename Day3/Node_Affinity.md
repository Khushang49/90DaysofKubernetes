Important Link:

https://kodekloud.com/topic/node-affinity-2/

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/7f2ff1bf-ac1c-496d-a5d1-1cea4c1fc9bc)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2dfb1226-2b23-43a8-85b6-48c4d86610be)


apiVersion: apps/v1

kind: Deployment

metadata:

  creationTimestamp: null
  
  labels:
  
    app: blue
    
  name: blue
  
spec:

  replicas: 3
  
  selector:
  
    matchLabels:
    
      app: blue
      
  template:
  
    metadata:
    
      creationTimestamp: null
      
      labels:
      
        app: blue
        
    spec:
    
      containers:
      
      - image: nginx
      
        name: nginx
        
        resources: {}
        
      affinity:
      
        nodeAffinity:
        
          requiredDuringSchedulingIgnoredDuringExecution:
          
            nodeSelectorTerms:
            
            - matchExpressions:
            
              - key: color
              
                operator: In (In,NotIn,Exists,NotExists)
                
                values:
                
                - blue  

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/7ac6f639-1c7d-4582-8713-f8f093ebf9cf)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/8bfb5203-9785-4c00-9f28-9cdbb92a8999)

