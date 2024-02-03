**Node Selector is only used when you want to create Pods in specific Node.** At that time we need to use Node selector. But for this you need to first label the node. Then only you can use node selector.

Sytax

apiVersion: v1
kind: Pod
metadata: 
  name: Testpod
  labels:
    name: test
    env: prod
spec:
  containers:
    - name: testcontainers
      image: ngnx
    **nodeSelector:**
      harware: test
      
