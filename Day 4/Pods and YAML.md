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

        ports:
          - containerPorts: 80
          
        restartPolicy: never  


  How to Create Pod from YAML?

 **kubectl create -f pod.yaml**

  or

  **kubectl apply -f pod.yaml**

  Create a POD YAML

  Go to VI editor

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/767c3db0-41bb-4374-8eca-310dc9aef277)

If you are having VS code then install YAML extension for better practice.

To check  YAML of POD

**#kubectl get pod -o yaml**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/37662870-35e0-4931-a582-13fd52f4dac6)

To copy in this file in YAML 

**#kubectl run nginx --dry-run=client -o yaml > test.yaml**

(Dry run mode gives you the possibility of issuing a command without side effects for testing an actual command that you intend to run.)

OR 

**#kubectl run nginx -o yaml > test.yaml**

Difference between create and apply

If you are editing any pod using edit command then these changes will be not update by create command you have apply those changes.

**#kubectl edit po podname**
