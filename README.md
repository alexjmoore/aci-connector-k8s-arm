# aci-connector-k8s-arm
Configuration files to deploy ACI Connector for Kubernetes on an ARM based environment.

Specifically the Raspberry PI 3 when using the kubeadm style deployment.

For more information, please see: https://github.com/Azure/aci-connector-k8s

## Dockerfile

Updated Dockerfile for the ACI Connector to use an ARM based image, note this also required NodeJS and NPM packages to be installed - there may be better base images to use.

## aci-connector-rbac.yamp

Kubeadm comes with K8s RBAC enabled by default, so this deployment defines a Role and a ClusterRole with required permissions and binds them to a ServiceAccount.

## aci-connector-arm.yaml

This is an updated deployment for the aci-connector itself, referencing the ARM based image on Docker Hub and the required service account defined above.
