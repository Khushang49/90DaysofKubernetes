What is Kubernetes?

Kubernetes basically a orchestrating tool for container. Kubernetes basically provide Autohealing as well as autoscaling.

There are two type of Application:

1.Monolith

2.Microservices

Monolithic Application:

My whole application will be in single code. Means If you want to add any changes any application then you have to do changes on whole code.

Microservices Application:

Here we create diffrent service for every functionallity.

Kubernetes Architecture

below diagram is kubernetes architecture diagram.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/147de780-0b79-4965-b2a8-0341d7d7f5e2)

**MASTER NODE :**

**API SERVER** :

Api server is main part for any request. Whenever user will send anything it will go via API server. It will take any request. 

Mainly all pods communicate with API server. We applu YAML to API server to craete pods as per our application.

It always scale as per our request or load.

It also help in authorization and authentication of user.

**CONTROL MANAGER** :

It will manage processes. If any pod ask for 4 container then it will check for actual state to desired state. Control manager get this data from ETCD.

In cloud we will have cloud control manager and for bare metal kube control manager.

**Components of Control manager:**

**Node Controller**:

It will check how many nodes are responding and which are not responding.

**Route Controller**:

It will help to set the networking and routes withing nodes and pods.

**Service Controller**:

If you are having load balancer as service then it will controll LB traffic and its rules.

**Volume Controller** :

It will controll volume creation and its mounting.

**ETCD** :

etcd is type of database which stores data of current states of pods. It is not part of kubernetes. The data will be as how manay pods will be there in pods. **Only API  server can access.** 

It stores metadata of cluster which is in key: value format. It is consistant and hoghly available.

Entire state is available on all nodes. It can write data upto 10,000 per second.

**KUBE SCHEDULER** :

**Mainly all work will be done by kube scheduler. To make desire state to actual state will be done by kubescheduler. Example if any pod want extra container then it will ask kubescheduler to add these pods.**

Whenever user write manifest then it is always will be executed by kube scheduler. Maily pods creation and management.

It is also intelligent which cheks where pods are not created and create pods there.

**USER** :

if any user want to add extra pods then it will send request to API server. Then it will send it to Control manager.

**FLOW IF ANY POD REQUIRE EXTRA CONTAINER:**

**USER (will mention YAML to add any pods) ---> API SERVER (Send to check state) ---> CONTROL MANAGER (Ask API to check state from ETCD) ---> API Server (Send to ETCD)**
**---> ETCD (It will send Actual State to API) ---> API Server (It will send Actual state to Control manager) ---> Control manager ( It will match with Desired state)** 
**---> API ( As we require extra pods) ---> Kubescheduler (It is main part who will work on request) ---> API Server (It will send it to Worker node)**  


**WORKER NODE :**

**CONTAINER ENGINE (DOCKER)** :

This will use as container engine who will create container inside pods. Ex. Docker, Rocketd etc.

**PODS** :

It is smallest part of kubernetes. kubernetes always communicate with Pods not with container. Also pods will have IP container will not have IP. As per standards wee need to keep one container per pod. But we can keep multiple also. But if single container goes in failed then all container will also goes down which cause issue with pod. **If any pod goes down then it will create new pod.** 



**KUBELET** :

It mainly manage pods. If any pod require any extra resources then it will ask kublet as kublet manage all pods. it will send this request to API Server. then it will send to control manager for desired state.

It is only which listens to master and sends data to API server and CControl manager.

It works on port 10255.

Mainly all working of pods send to Master(Control Manager).

**KUBEPROXY** :

Kubeproxy assigns IP to pods. It is dynamic in nature means on restart IP will change.

**CNI** :

These all are bounded by CNI. Container network interface.


Important:

Kubectl : Cloud

Kubeadm : Linux server

kubefed : for Hybrid
