What is Deployment?

It is above replicaset. It is also object. Deployment manages replicaset. 

Deployment maintains the replicaset version. If you create replicaset as V1 version then you done some chnges then it will create as V2. 

**If you increace PODS and then try rollout with decrease in Pod then it will have same POD as that current version. It will not reduce.**

Still replicaset will create POD. But Replicaset will be managed by Deployment. Basically it will help for version controlling of your application.

**Whenever you create new version then it will delete old replicaset and pods.**

If there is any problem with deployment then kubernetes automatically roll back to older version.



![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/80a820dd-2ea5-49af-9ad0-721e8de1b58a)

