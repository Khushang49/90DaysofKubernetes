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
