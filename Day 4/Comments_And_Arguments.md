Meaning of command and argumrnt is to run any command while create container.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/aabbe1fc-c161-4a4a-8960-cd522089a40c)

In last example in commmand we mention /bin/sh === this is for shell

in argument -c is for command and next will be the value which need to perform.

Syntax of command and argumemnt

command: [""]

args: [""]

If you mention any command or enrtrypoint in DOckerfile but you mention command and argument in yaml then it will run yaml command first.

If you want to mention any command while running pod.

kubectl run podname --image=imagename --command -- argument(key)=value



Quetions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/97291692-e892-4285-b93f-375f79731a2e)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/52345de1-b6a2-4aee-a6f6-e277dea19ffc)


Solution: 

````
apiVersion: v1 
kind: Pod 
metadata:
  name: ubuntu-sleeper-2 
spec:
  containers:
  - name: ubuntu
    image: ubuntu
    command:
      - "sleep"
      - "5000"
`````   

OR

```
apiVersion: v1 
kind: Pod 
metadata:
  name: ubuntu-sleeper-2 
spec:
  containers:
  - name: ubuntu
    image: ubuntu
    command: [sleep]
    args: ["5000"]
```


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ed487561-c7e3-46bd-8903-09d0fa468637)

```
apiVersion: v1 
kind: Pod 
metadata:
  name: webapp-green
  labels:
      name: webapp-green 
spec:
  containers:
  - name: simple-webapp
    image: kodekloud/webapp-color
    args: ["--color", "green"]
```


how to edit file which is edited via kubectl edit?

**#kubectl replace --force -f /tmp/kubectl.yml**
