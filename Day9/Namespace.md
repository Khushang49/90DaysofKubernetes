https://kodekloud.com/topic/namespaces/

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ecf43b0d-9851-48c2-97eb-d4b2adcec4c8)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/26683861-d78f-4bf7-bb44-10830890e9be)

How Pods will access any po which is in different namespace?

it will access with the help of URL: **podname.namespace.svc or pod.cluster.local**

If it is in same namespace then it will access with the help of name of POD.

Commands:

**#kubectl get ns --no-headers | wc -l**

**#kubectl get pods --all-namespaces**

Questions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/48882067-8319-4154-8b58-fc570a0f6b60)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ce9aaee3-e16a-4157-9e5d-8ccc4e49f1d7)

**#kubectl run redis --image redis --namespace finance**
