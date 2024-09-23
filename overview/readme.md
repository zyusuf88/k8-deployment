# Kubernetes Overview

Kubernetes (K8s) is a powerful container orchestration platform that helps manage containerized applications in various environments. It simplifies deploying, scaling, and operating applications.

## Key Features

- **High availability**: Ensures no downtime.
- **Scalability**: Automatically scales applications based on demand.
- **Disaster recovery**: Provides backup and restore capabilities via ETCD snapshots.

## Why Do We Need Kubernetes?

With the shift from monolithic to microservices and the increased use of containers, there is a need for a proper orchestration tool to manage hundreds or thousands of containers. Kubernetes helps by:

- Managing containerized workloads across different environments.
- Ensuring that applications are highly available and scalable.

## Kubernetes Architecture

Kubernetes clusters consist of at least one **Master Node** and multiple **Worker Nodes**:

- **Master Node**: Contains the essential components to manage the cluster:
  - **API Server**: Handles internal and external requests.
  - **Controller Manager**: Manages the state of the cluster.
  - **Scheduler**: Assigns workloads to worker nodes.
  - **ETCD**: Stores the cluster's state as key-value pairs, enabling recovery.

- **Worker Nodes**: Run your application and have Kubernetes processes running on them:
  - **Pods**: The smallest deployable unit in Kubernetes, which contains the container(s) for your application.
  - **Kubelet**: The process running on worker nodes to communicate with the Master node.

## Networking in Kubernetes

- Kubernetes uses a **virtual network** to connect nodes and allow pods to communicate internally using their own IP addresses.
- Kubernetes Services act as a stable interface to expose the application (pods), as pods are frequently recreated, and their IP addresses change.

## Kubernetes Services

A Kubernetes Service is used to expose your application through:

- **ClusterIP**: Internal access within the cluster.
- **NodePort**: Exposes the service on a port of the node, making it accessible externally.
- **LoadBalancer**: For external access via a cloud provider's load balancer.

### Features of Kubernetes Services

- **Permanent IP address**: For reliable communication between pods.
- **Load balancing**: Distributes traffic between pods.

## Additional Resources

- [Kubernetes Official Documentation](https://kubernetes.io/docs/)
- [Minikube Documentation](https://minikube.sigs.k8s.io/docs/)