Why we require Monitoring?

We require monitoring to monitor our Nodes and Pods basis on CPU and Memory. Kubernetes doesnot come with any monitoring solution. You need to configure this solutions.

**Metric server** is used to monitor the Kubernetes cluster. Also it does not store this data. It is only used for for live monitoring.

git clone https://github.com/kodekloudhub/kubernetes-metrics-server.git

**#kubectl create -f .** ( to run all yaml files)

**#kubectl top nodes**  (to check nodes memory)

**#kubectl top pods**  (to check memory of pods)

**#kubectl logs -f podname** or **#kubectl logs -f podname -c containername**  (to check logs of pod)

Also If you want store the logs then just mention container name after your pod defination.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/327746fb-48cf-447d-9af9-e04f3dcca36a)
