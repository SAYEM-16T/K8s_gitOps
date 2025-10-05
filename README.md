# K8s GitOps with KinD

This repository contains Kubernetes manifest files for managing a sample application deployment on a KinD (Kubernetes in Docker) cluster using GitOps principles.

## Directory Structure

```
.
├───.git/...
└───gitops/
    ├───auth-deployment.yaml
    ├───auth-service.yaml
    ├───frontend-deployment.yaml
    ├───frontend-service.yaml
    ├───mongo-deployment.yaml
    ├───mongo-service.yaml
    └───namespace.yaml
```

## File Descriptions

*   `auth-deployment.yaml`: Defines the desired state for the authentication microservice, such as the container image, number of replicas, and resource limits.
*   `auth-service.yaml`: Creates a stable network endpoint to expose the authentication microservice to other components within the cluster.
*   `frontend-deployment.yaml`: Defines the deployment for the user-facing frontend application pods.
*   `frontend-service.yaml`: Exposes the frontend application, often to external traffic, so users can access it.
*   `mongo-deployment.yaml`: Defines the deployment for a MongoDB database instance, which likely serves as the backend database.
*   `mongo-service.yaml`: Creates a stable internal network endpoint for other services to connect to the MongoDB database.
*   `namespace.yaml`: Defines a Kubernetes Namespace to create an isolated environment for all the application's resources to run within.