What is deployment strategies?

Whenever we want to deploy our application as per deployment strategies such as recreate and rolling update. By default on deployment rolling update is configured.

Meaning of this strategies are whenever we change update our deployment then we need to mention how my pods should take update.

**In recreate it will destroy all pods and try to create new one pod one by one.**

**In rolling update it will check the strategy if it is mentioned 25% and deployment has 4 replicas then it will check on 1 pod first if application is working fine then only it will use that deployment. otherwise it will give error.**

Below mentioned are strategies of deployment.

**Recreate**

**Rollback**

**Rollout**

**Rollingupdate**
