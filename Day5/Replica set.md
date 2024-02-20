What is Controller?

Controler are the brain behind Kubernetes.

What is Replication Controller?

We require replication to make our application to highly available.

You can have replication controller on single pod also.

There are two types of replication mechanism.

1. Replication controller
2. Replica Set

Difference between replication controller and replicaset

replication controller supports only equality based selcetor 

wheras replicaset supports both equality as well as set based.

Equality based means it will use only one label where as set based will have multiple labels to choose.

YAML for Replication Controller:

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/8f47c8a9-0f18-4052-8dac-b1e152a9d5b3)

OR

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/04c2abef-250e-4e48-b490-43349e0bc208)

YAML for ReplicaSet

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/72fa970f-017c-4ea2-887a-e067747d4f98)

We cant add matchLabels or matchexpression in ReplicationController as it will only use for single 

 selector:
    
    matchLabels:
       
       type: prod
	   
	   OR
  selector:
   
    matchExpressions:	  
       
       - {key: env, operator: in,notin,exist value: [test]}

 **Matchlabels and MatchExpression will only match labels which mentioned in pod LABEL.**


How you will scale this replicas? Below Logic will be used for both Replication controller as well as replicas set.** Also This will not change in YAMl.**

1. By changing number in replicas in YAML.

2. By mentioning in command.

**#kubectl scale --replicas=5 -f rs.yml**

Syntax: **kubectl scale --replicas=desired number -f yamlname**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/ee658df8-b40b-4e63-afcc-2ed902ce61d0)

3. By mentioning command
   **#kubectl scale --replicas=1 replicationcontroller rc1**
   
   Syntax: **kubectl scale --replicas=1 replicationcontroller replicationcontrollername**
    
 ![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/4071226b-6754-4987-a678-bcf7525975c7)

   
