1.
![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/3931edae-a7dc-48ce-abf1-2a3f85bd3785)

Imperactive Method:

Create Deployment

**#kubectl craete deployment nginx --image=nginx**

Set the Image to specific image

**#kubectl set image deployment/nginx nginx=nginx:1.19.8**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/06107a10-4674-4218-851c-45fd91047ab6)


2.
![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/a60a4b1f-68d7-485b-a29b-89d1dd26a4ae)

Static POD path is used to store kubelet configuration. How to check config?

**#ps -aux | grep kubelet**

**ps -aux is used To see every process on the system. Highlighted one is config file path.**

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/790b546a-d4fd-456b-86f6-be8aa9c10d37)

Now view this path 

![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/35f9d390-bb25-4fa5-b425-991a2e91a45c)

Just edit and add the required path.

3.
![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/2bb88181-2f5a-4b3b-9cf4-5e76b47d3064)


4.
![image](https://github.com/Khushang49/90DaysofKubernetes/assets/95266353/e888701e-6a8d-47b6-820d-dbf9a3c31869)

**#kubectl get pods --show-labels | grep finance | wc -l**







