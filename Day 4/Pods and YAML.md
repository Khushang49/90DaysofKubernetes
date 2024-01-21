Pods basically contain 4 top level field

**apiVersion:**
**kind:**
**metadata:**


**spec:**

**apiVersion values and Kind values:**

Basically keep v1. For Kind always keep first letter capital. You have to mention spaces properly. Best practice is to keep 3 to 4 spaces to parent.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/be68def2-ba41-48aa-9ca2-92ce52bd7eeb)

metadata values:

You can only mention **name and Label**.

name: any name

labels:
   
    name: any name
    
    enviroment: prod
    
    type: backend

Spec values:

spec: 

   container: 
   
      - name: nginx(container name)
      
        image: nginx


  How to Create Pod from YAML?

  kubectl create -f pod.yaml

  or

  kubectl apply -f pod.yaml
