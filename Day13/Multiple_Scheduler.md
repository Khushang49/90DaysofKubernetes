https://www.youtube.com/watch?v=NiB7sjXmiZc&t=122s

https://kodekloud.com/topic/multiple-schedulers/


Basically Scheduler do below tasks 

1) Filtering the nodes

2) Ranking the nodes.


If you are creating custom scheduler you can create with the help of YAML of kube scheduler. Which can be found in in **/etc/kubernetes/manifests**. Also Kube-scheduler works on **10259** port

Change and add below points in parameter

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/311e5543-96a5-4782-bbd1-aff34004d9c0)


1)First if you are creating custom scheduler then change value of parameter. This will be true when you have multiple nodes and you want single scheduler to work.

**- --leader-elect=false (which was true)**

2) Now add schedular name
   **- --scheduler-name=testscheuler** **(same should be there in name of metadata)**

3) Port addition on which my scheduler will work. It has to be unique. You need to mention different port which is not in use. check port **( netstat -tunlp | grep 10358)**. Change port from Liveness probe also.

   **- --port=10258**

   ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/a15faa1f-907b-44b8-aa9c-397c3556184c)


5) Now mention secure port.The port on which to serve HTTPS with authentication and authorization. If 0, don't serve HTTPS at all.

  **- --secure-port=0**

How to mention Custom Scheduler in Pod. Just mention in spec of POD.

**schedularName: name**

Also for checking just describe the POD and check in event.
