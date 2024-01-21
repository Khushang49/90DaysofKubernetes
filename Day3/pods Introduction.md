What is Pod?

Pod is smallest unit or object created in Kubernetes. Container are encapsulated in POD. To scale up you craete new pod and to scale down you delete pod.

You can deploy multiple container in single pod but if any one container goes down then pod goes in failed state.

If you deploy multiple contaner in single pod then they will use same network and communicate as **LocalHost** . Also they use same storage.

**A POD is singleinstance of application.**

Hoe to deploy POD??

#**kubectl run nginx --image nginx**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ed858d91-ec17-41c4-8868-f93c77038db5)



How to check Pods created??

**#kubectl get pods**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/d8627997-ae83-4b9d-82ea-891f70333c29)


How to access the pods??

**#kubectl exec -it podname -- sh**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e627d950-dcf4-47ed-b03d-65230c0898b4)


How to Describe to get details regarding IP and everything??

**#kubectl describe pod podname**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/3147b1ce-615f-486c-b94c-ee0917db7e46)

**#kubectl get pods -o wide**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/941cfec6-df92-4c29-b6f5-44bbe01ade10)

 
