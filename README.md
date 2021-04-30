# Notes

## General
**Cluster**
- Control Plane + Nodes

**Namespaces**
- virtual clusters backed by the same physical cluster
- a way to divide cluster resources between multiple users

**Controllers**
- control loops that watch the state of your cluster, then make or request changes where needed
- each controller tries to move the current cluster state closer to the desired state

**Node**
- physical or virtual machine running Kubernetes services
- components: kubelet, container runtime, kube-proxy

**Pod**
- a group of one or more containers that share the same storage space and the same network resources
- each pod has a single ephemeral IP address which is shared by all containers running within the Pod
- "one-container-per-Pod" model is the most common Kubernetes use case > a wrapper around a single container
- Kubernetes manages Pods rather than managing the containers directly

**Workloads**
- apps running on Kubernetes
- built-in workload resources: Deployment, RepicaSet, StatefulSet, DaemonSet, Job, CronJob

**Deployment**
- a tool that manages the performance and specifies the desired behavior of a pod
- specifies the application’s life cycle, including the pods assigned to the app
- good fit for managing a stateless application workload on your cluster- creating/deleting a deployment automatically creates/deletes it's pod; don't create/delete pods separately

**Service**
- an abstract way to expose an application running on a set of Pods as a network service
- an abstraction which defines a logical set of Pods and a policy by which to access them
- the set of Pods targeted by a Service is usually determined by a selector
- most commonly abstract access to Kubernetes Pods