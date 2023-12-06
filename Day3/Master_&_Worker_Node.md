After installation of Minikube. Just check for container. This will be master node and worker node. It will have all components which we seen in Architecture of Kubernetes. 

**#docker ps**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/96d61ece-31aa-4024-a92e-41482a484b03)

Now go inside this minikube container to verify the components of K8S.

**#minikube ssh**

and list container you will able to see all containers.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ca042d0b-0b9f-441b-8536-d6fbcff402b1)

Basically it create multiple container of these components of K8S. Basically these pods help K8S to scale these pods as per requirement.




