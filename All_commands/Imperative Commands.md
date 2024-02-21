![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/7ce9746d-03e3-4987-b6dc-c81f58b8c466)

POD Creation Command

**#kubectl run nginx-pod --image=nginx:alpine --restart=Never --port=80**

**#kubectl run redis --image=redis:alpine -l tier=db**

Create a service redis-service to expose the redis application within the cluster on port 6379.

**#kubectl expose pod redis  --port=6379 --name redis-service**

Deployment Creation Command

Create a deployment named webapp using the image kodekloud/webapp-color with 3 replicas.

**#kubectl create deploy webapp --image=kodecloud/webapp-color --replicas=3**

Create a new deployment called redis-deploy in the dev-ns namespace with the redis image. It should have 2 replicas.

**#kubectl create deployment redis-deploy --namespace dev-ns --image=redis --replicas=2**

Service Creation Command:

Create a pod called httpd using the image httpd:alpine in the default namespace. Next, create a service of type ClusterIP by the same name (httpd). The target port for the service should be 80.

**#kubectl run httpd --image=httpd:alpine --port=80 --expose**

OR

**#kubectl run httpd --image=httpd:alpine and #kubectl expose po httpd --type=ClusterIP --port=80**

Namespace Creation Command:

Create a new namespace called dev-ns.

**#kubectl create ns dev-ns**
