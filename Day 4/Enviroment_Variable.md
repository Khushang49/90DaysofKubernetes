Why Enviroment varaible used?

If we want pass any value for code at that time we use this enviroment variable.

There are two types to mention these enviroment variable.

1 env: 
   - name:
     value:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/b9fc95a7-576b-4767-b82b-cfa92df16ac8)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2bd665f7-a043-4c84-9b0e-9a136914599c)


2. envFrom:




Questions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/30f4ada4-6040-4cd9-b2ed-c41e39235ca5)

```
apiVersion: v1
kind: Pod
metadata: 
  name:  testenv
spec: 
  containers: 
    - name: testenv 
      image: webapp-color
      env: 
        - name: APP_COLOR
          value: green
```
