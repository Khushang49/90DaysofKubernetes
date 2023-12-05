Create 3 VM 1 as worker and other 2 as worker.

**For this all master as well as worker need to be in same subnet.**

Also on all VM port 22 need to enabled or ssh service as we can easily take putty of this VM.

#sudo apt install openssh-server

Whenever you install kubernetes always off Swap memory.

As an orchestration tool, Kubernetes operates on the design principle that deployments should use as close to 100 percent of resources as possible, to maintain efficiency. The Kubernetes scheduler determines the best available node on which to deploy newly created pods. If memory swapping is allowed to occur on a host system, this can lead to performance and stability issues within Kubernetes. For this reason, Kubernetes requires that you disable swap in the host system.

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

#apt-get update 

#apt install docker.io

Also check which version will be supported by kubernetes Or check the documentation to install docker.

Now install kubeadm to your nodes.

1. Check the MAC whetehr it is legit as we cant use snapshoted VM or Hardcloned VM.

   #sudo cat /sys/class/dmi/id/product_uuid





