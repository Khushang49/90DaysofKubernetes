Important Links:

https://www.youtube.com/watch?v=y4UarwGKZQQ

https://kodekloud.com/topic/taints-and-tolerations-2/

What is taints?

So basically if you want to craete PODS in specific Node then we have to mention these Taints first on Node and Toleration parameter should be there in Pod.

**Mainly our Control Plane Node has this feature. hence we cannot craete pods on Control Plane. Also It dosent mean pod which has toleration pod will only scheduled at that node it can go to any node.**

There are three effects are there NoSchedule, PreferNoSchedule,NoExecute

**NoSchedule: It will not schedule new pods on that node.**

**PreferNoSchedule: It will try to schedule on this node but cant confirm**

**NoExecute: It remove all pods which were scheduled before by removing those pods.**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/8a134052-f6a8-48eb-8213-b8c68ea15a44)


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/fc539c32-6e4c-43f4-b15a-059efcaf91d8)


![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2ab43be3-8dd7-48a6-93ae-6e9a8eb37bc2)


Quetions:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/4b49adcf-7ee7-46e2-b77b-2eeaf21efb2c)

1. First apply taint on node

   Check node and apply taint

   **#kubectl get nodes**

   **#kubectl taint node nodename color=blue:NoSchedule**

   ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/b7e38f90-5af0-4214-b54e-65faa52afdbe)

   How to check whether taints are applied or not.

   **#kubectl describe node nodename | grep taint**

   ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/25875a63-3f19-4428-866c-d72a0b16cdd7)

2. It will not run and find different node for running.

3. First Create Pod and create YAML

   **#kubectl create nginx --image=nginx --dryn-client=client -o yaml > first.yml**

   Then add toleration part in POD:

   Syntax for toleration:

   **tolerations:**
     **- key: "color"**
       **operator: "Equal"**
       **value: "blue"**
       **effect: "NoSchedule"**

   ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e4a93e18-be9a-448f-ad4d-b87e1edca700)

   To Check Pod status

  **#kubectl get pods**

4. To remove taints from node just mention - at end of command

   **#kubectl taint node nodename color=blue:NoSchedule**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/fe898fba-c764-4e5a-94fe-d03bdd214f22)

