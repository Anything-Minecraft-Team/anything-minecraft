# K3s Simple Setup

> Due to the various versions of kubernetes references below will be focused on deploying to a [k3s.io] cluster. If you want information on how to spin up a cluster please check out the [k3s.io] link.

[k3s.io]: https://k3s.io/

## Getting started

### Creating the project

1. First we want to set up a project folder. Please create one and open it with your favorite text editor.
2. Copy the contents of this directoy into your project directory.

### Spin-up

> This will create the resources!

```sh
# We create the namespace first always before we spin up.
kubectl apply -f ./base/01-namespace.yml

# Now we can spin everything up.
kubectl apply -k .
```

### Spin-down

> This will remove all resources!

```sh
kubectl delete -k .
```

---

### Breakdown

#### [Namespace](./base/01-namespace.yml)

This drives where the deployment will be filed under. Its best practices to segement each deployment in its own namespace. [Namespace documentaion can be found here](https://kubernetes.io/docs/tasks/administer-cluster/namespaces/#creating-a-new-namespace)

#### [Kustomization](./kustomization.yml)

The kustomization file is used to build a project and correlate data across multiple files. If you are looking for more details on [documentation for kustomization click here](https://kubectl.docs.kubernetes.io/guides/introduction/kustomize/).

#### [Persisted Volume Claim](./base/02-pvc-config.yml)

This is where your data is stored! It contains all data pertaining to your minecraft server and should be backed up! As a recommendation [take a look at Velero](https://velero.io/). However, if you are looking for [more information on persisted volume claims click here](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)

#### [Deployment](./server/01-deployment.yml)

The deployment is what actually spins up your server and its related content. You can get more advanced with your deployment by adding additional environment variables, an admin panel, or other tools to help you administrait it. [More information on deployments can be found here](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)

#### [Join Service](./server/02-join-service.yml)

This provides the connection to your minecraft server! Its highly recommended to have a failover IP set as your external IP in a simple deployment. In a more advanced example you might want to have a proxy as your ingress if you are catering to multiple minecraft servers. [More information on services can be found here](https://kubernetes.io/docs/concepts/services-networking/)
