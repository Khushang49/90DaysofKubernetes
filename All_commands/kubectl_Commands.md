List of Kubernetes commands:

kubectl cluster-infokubectl: Get cluster information.

Kubectl get nodes: View all the node prestt in the cluster

Kubectl get nodes: List all the nodes

Kubectl describe node <node name>: Describe a specific node

Kubectl drain node: Drain a node for maintenance

For Creating Namespace

Kubectl describe namespace: Describe a namespace

Kubectl create namespace: Create a namespace

Kubectl get namespace: List all namespace

kubectl describe namespace <namespace-name>: Describe a namespace.

kubectl create namespace <namespace-name>: Create a namespace.

kubectl get namespaces: List all namespaces.

kubectl config set-context –current –namespace=<namespace-name>: Switch to a different namespace.

kubectl delete namespace <namespace-name>: Delete a namespace.

kubectl edit namespace <namespace_name>: Edit and update the namespace definition.

For Creating Resources

kubectl apply -f <resource-definition.yaml>: Create or Update a resource from a YAML file.

kubectl create: Create an object imperatively.

kubectl apply -f https://url-to-resource-definition.yaml: Create a resource by using the URL.

For Viewing and Finding Resources

kubectl get <resource-type>: List all resources of a specific type.

kubectl get <resource-type> -o wide: List all resources with additional details.

kubectl describe <resource-type> <resource-name>: Describe a specific resource.

kubectl get <resource-type> -l <label-key>=<label-value>: List all resources with a specific label.

kubectl get <resource-type> –all-namespaces: List all resources in all namespaces.

kubectl get <resource-type> –sort-by=<field>: List all resources sorted by a specific field.

kubectl get <resource-type> -l <label-selector>: List resources with a specific label selector.

kubectl get <resource-type> –field-selector=<field-selector>: List resources with a specific field selector.

kubectl get <resource-type> -n <namespace>: List all resources in a specific namespace.

For Deleting Resources

kubectl delete <resource-type> <resource-name>: Delete a resource.

kubectl delete <resource-type1> <resource-name1> <resource-type2> <resource-name2>: Delete multiple resources.

kubectl delete <resource-type> –all: Delete all resources of a specific type.

kubectl delete -f <resource-definition.yaml>kubectl delete -f https://url-to-resource-definition.yaml: Delete the resource by using url.

kubectl delete <resource-type> –all -n <namespace>: Delete all resources in a specific namespace.



List 2 of Kubernetes commands:

For Copying Files and Directories

kubectl cp <local-path> <namespace>/<pod-name>:<container-path>: Copy files and directories to a container.

kubectl cp <namespace>/<pod-name>:<container-path> <local-path>: Copy files and directories from a container.

kubectl cp <namespace>/<pod-name>:<source-container-path> <destination-namespace>/<destination-pod-name>:<destination-container-path>: Copying files from one container to another within the same pod.

kubectl cp <namespace>/<source-pod-name>:<source-container-path> <destination-namespace>/<destination-pod-name>:<destination-container-path>: Copying files from one container to another in a different pod.

For Patching Resources

kubectl patch <resource-type> <resource-name> -p ‘<patch-document>: Patch a resource using a JSON or YAML document.

kubectl patch <resource-type> <resource-name> –patch-file=<patch-file>: Patch a resource using a JSON or YAML file.

For Scaling Resources

kubectl scale deployment <deployment-name> –replicas=<replica-count>: Scale a deployment.

kubectl scale statefulset <statefulset-name> –replicas=<replica-count>: Scale a statefulset.

kubectl scale replicaset <replicaset-name> –replicas=<replica-count>: Scale a replica set.

For Pod Management

kubectl create -f <pod-definition.yaml>: Create a pod from a YAML file.

kubectl get pods: List all pods in the cluster.

kubectl describe pod <pod-name>: Describe a specific pod.

kubectl logs <pod-name>: Get logs from a pod.

kubectl logs -f <pod-name>: Stream logs from a pod.

kubectl logs -l <label-key>=<label-value>: Get logs with a specific label.

kubectl exec -it <pod-name> — <command>: Exec into a pod.

kubectl delete pod <pod-name>: Delete a pod.

kubectl create pod <pod-name>: Create a pod with the name.

kubectl get pod -n <namespace_name>: List all pods in a namespace.

For Deployment Management

kubectl create deployment <deployment-name> –image=<image-name>: Create a deployment.

kubectl get deployments: List all deployments.

kubectl describe deployment <deployment-name>: Describe a specific deployment.

kubectl scale deployment <deployment-name> –replicas=<replica-count>: Scale a deployment.

kubectl set image deployment/<deployment-name> <container-name>=<new-image-name>: Update a deployment’s image.

kubectl rollout status deployment/<deployment-name>: Rollout status of a deployment.

kubectl rollout pause deployment/<deployment-name>: Pause a deployment rollout.

kubectl rollout resume deployment/<deployment-name>: Resume a deployment rollout.

kubectl rollout undo deployment/<deployment-name>: Rollback a deployment to the previous revision.

kubectl rollout undo deployment/<deployment-name> –to-revision=<revision-number>: Rollback a deployment to a specific revision.

kubectl delete deployment <deployment-name>: Delete deployment name.

List 3 of Kubernetes commands:

ReplicaSets Management
```
kubectl create -f <replicaset-definition.yaml>: Create a ReplicaSet.
kubectl get replicasets: List all ReplicaSets.
kubectl describe replicaset <replicaset-name>: Describe a specific ReplicaSet.
kubectl scale replicaset <replicaset-name> –replicas=<replica-count>: Scale a ReplicaSet.
```
Service Management
```
kubectl create service <service-type> <service-name> –tcp=<port>: Create a service.
kubectl get services: List all services.
kubectl expose deployment <deployment-name> –port=<port>: Expose a deployment as a service.
kubectl describe service <service-name>: Describe a specific service.
kubectl delete service <service-name>: Delete a service.
kubectl get endpoints <service-name>:  Get information about a service.
```
Config Maps and Secrets
```
kubectl create configmap <config-map-name> –from-file=<path-to-file>: Create a config map from a file.
kubectl create secret <secret-type> <secret-name> –from-literal=<key>=<value>: Create a secret.
kubectl get configmaps: List all config maps.
kubectl get secrets: List all secrets.
kubectl describe configmap <config-map-name>: Describe a specific config map.
kubectl describe secret <secret-name>: Describe a specific secret.
kubectl delete secret <secret_name>: Delete a specific secret.
kubectl delete configmap <config-map-name>: Delete a specific config map.
```
Networking
```
kubectl port-forward <pod-name> <local-port>:<pod-port>: Port forward to a pod.
kubectl expose deployment <deployment-name> –type=NodePort –port=<port>: Expose a deployment as a NodePort service.
kubectl create ingress <ingress-name> –rule=<host>/<path>=<service-name> –<service-port>: Create an Ingress resource.
kubectl describe ingress <ingress-name>: Get information about an Ingress.
kubectl get ingress <ingress-name> -o jsonpath='{.spec.rules[0].host}’: Retrieves the most value from the first rule of the specified Ingress resource.
```
Storage
```
kubectl create -f <persistent-volume-definition.yaml>: Create a PersistentVolume.
kubectl get pv: List all PersistentVolumes.
kubectl describe pv <pv-name>: Describe a specific PersistentVolume.
kubectl create -f <persistent-volume-claim-definition.yaml>: Create a PersistentVolumeClaim.
kubectl get pvc: List all PersistentVolumeClaims.
kubectl describe pvc <pvc-name>: Describe a specific PersistentVolumeClaim.
```
StatefulSets
```
kubectl create -f <statefulset-definition.yaml>: Create a StatefulSet.
kubectl get statefulsets: List all StatefulSets.
kubectl describe statefulset <statefulset-name>: Describe a specific StatefulSet.
kubectl scale statefulset <statefulset-name> –replicas=<replica-count>: Scale a StatefulSet.
```
Monitoring and Troubleshooting
```
kubectl get events: Check cluster events.
kubectl get component statuses: Get cluster component statuses.
kubectl top nodes: Get resource utilization of nodes.
kubectl top pods: Get resource utilization of pods.
kubectl debug <pod-name> -it –image=<debugging-image>: Enable container shell access debugging.
```
