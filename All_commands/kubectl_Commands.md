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
