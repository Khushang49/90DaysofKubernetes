Important Links:

https://kodekloud.com/topic/resource-limits/


Resource Limit:

It is used to provide memory and cpu to the POD.

Syntax:

resources:

  requests:
  
    cpu: 1
    
    memory: "1Mi"

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/270fcd2c-93c6-4121-8c49-9294389f1398)


Also we can set the limits also
syntax

resources: 

  requests:
  
    cpu: 1
    
    memory: "1Mi"
    
  limits:
  
    cpu: 2
    
    memory: "2Mi"

  ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/faae4dfe-0230-4455-9ab6-0b38e1b53f68)


If pod request more than the memory then it will ho to OOM( out of memory). Just describe Pod and check in state parameter.


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/639842b9-b76c-4588-811e-50a8974dca18)
