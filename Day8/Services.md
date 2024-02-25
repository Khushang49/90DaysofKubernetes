**Services**

**Services are created only connect your application outside of the network or Inside the network on specific IP. Because when you create replicaset it will create multiple IP so we cannot every IP thats why we have services. Because everyone will not have details of pod IP's.**

There are three services.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/425b431d-fb94-42d1-94f7-b9a00af478cf)


Node Port:

Node Port is used to enable node Port to external user to access the application. It will work on port from 30000-32767



![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e2b70ce0-867a-4937-9dae-2739447dbfcd)

Cluster IP:

It is used to provide specific IP in Cluster to connect. As deployment will have multiple pods. Hence it will provide specific IP to that deployment.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/dccbb440-ebb9-40a5-99f5-aedadc85feee)

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2196ca9e-9c11-4fe5-b215-37d5e8967a2a)


Load Balancer:

In Node port it will be configured on single Port But if we have Load Balancer then we use this as Single IP for our application.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/5e62afe5-5855-4a78-a64d-954ce7ab05c0)

Questions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/b5af6033-cae5-4b3f-8ad8-6849036dfd6e)


