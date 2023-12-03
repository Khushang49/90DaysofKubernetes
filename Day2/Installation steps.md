Create 3 VM 1 as worker and other 2 as worker.

Whenever you install kubernetes always off Swap memory.

How to check whether swap is on:

**#free -h**

If you able to memory at swap means swap is enabled.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/89e0fb44-3350-4561-b543-814e2a6e7fcb)

How to disable swap on server

**#swapoff -a**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e94e0398-9765-429f-98a3-18a7f27bbc87)

If you want to disable swap memory permanently. Then comment all line in fstab which is related to swap. Just go to /etc/fstab and disable the swap permanently.

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/fbf55d6d-ab0e-4388-b43a-42bc0122f9bd)

Kubernetes require any container engine to be installed. hence we can use any one of Container engine. Such as docker,rocket etc.

Also check which version will be supported by kubernetes.




