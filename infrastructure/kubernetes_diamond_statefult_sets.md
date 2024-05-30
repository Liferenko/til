# DeamonSet vs. Stateful set (K8s)

### Stateful set

formerly known as PetSet (before K8s 1.5, 2016)

Deployments and ReplicaSets - a great way to run stateless replicas of an application on Kubernetes.
Their semantics aren't really right for stateful application deployment.

StatefulSet provides a controller with proper semantics for deploying a wide range of stateful workloads


**ELI5 vesrion:**
ReplicaSet needs to manage pods. Every pod is interchangeable.
If a pod fails or removed, the controller replaces it to maintain desired number of replicas.
Pod's naming is generated
```
apiVersion: apps/v1
kind: ReplicaSet
    ...
```
---

StatefulSet is used for apps that requires stable, unique network ids and stable persist storage.
Behaviour: sticky identity for each pod. 
Pod's naming is user-provided and maintain their identity across restarts.

Source - https://kubernetes.io/blog/2016/12/statefulset-run-scale-stateful-applications-in-kubernetes/

---

DeamonSet
As nodes are removed from the cluster, those Pods are garbage collected. Deleting a DaemonSet will clean up the Pods it created.

```
apiVersion: apps/v1
kind: DaemonSet
    ...
```

