Kubernetes Architecture

below diagram is kubernetes architecture diagram.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/147de780-0b79-4965-b2a8-0341d7d7f5e2)

**MASTER NODE :**

**API SERVER** :

Api server is main part for any request. Whenever user will send anything it will go via API server. It will take any request. 

Mainly all pods communicate with API server. 

**CONTROL MANAGER** :

It will manage processes. If any pod ask for 4 container then it will check for actual state to desired state. Control manager get this data from ETCD.

**ETCD** :

etcd is type of database which stores data of current states of pods. It is not part of kubernetes. The data will be as how manay pods will be there in pods. **Only API  server can access.** 

**KUBE SCHEDULER** :

Mainly all work will be done by kube scheduler. To make desire state to actual state will be done by kubescheduler. Example if any pod want extra container then it will ask kubescheduler to add these pods.

**USER** :

if any user want to add extra pods then it will send request to API server. Then it will send it to Control manager.

**FLOW IF ANY POD REQUIRE EXTRA CONTAINER:**

**USER (will mention YAML to add any pods) ---> API SERVER (Send to check state) ---> CONTROL MANAGER (Ask API to check state from ETCD) ---> API Server (Send to ETCD)**
**---> ETCD (It will send Actual State to API) ---> API Server (It will send Actual state to Control manager) ---> Control manager ( It will match with Desired state)** 
**---> API ( As we require extra pods) ---> Kubescheduler (It is main part who will work on request) ---> API Server (It will send it to Worker node)**  


**WORKER NODE :**

**CONTAINER ENGINE (DOCKER)** :
