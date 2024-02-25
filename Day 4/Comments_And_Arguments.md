










Quetions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/97291692-e892-4285-b93f-375f79731a2e)

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
