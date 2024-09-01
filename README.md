# Weather Chart Kubernetes Manifests

This repository contains the Helm chart for deploying and managing the Weather Chart application on a Kubernetes cluster. The Helm chart includes various Kubernetes resources such as Deployments, Services, Ingress, HPA, and more.

## Repository Structure

```plaintext
├── templates/
│   ├── _helpers.tpl
│   ├── configmap.yaml
│   ├── deployment.yaml
│   ├── hpa.yaml
│   ├── ingress.yaml
│   ├── networkpolicy.yaml
│   ├── service.yaml
│   ├── serviceaccount.yaml
├── Chart.yaml
└── values.yaml
```

### Breakdown:

- **Chart.yaml**: Contains metadata about the Helm chart, such as the chart name, version, and description.
- **values.yaml**: Defines the default values for this Helm chart, which can be overridden during deployment.
- **templates/**: This directory contains the Kubernetes resource templates that Helm will render using the values from `values.yaml` or custom values provided during installation.
  - **_helpers.tpl**: A file containing template helpers that can be reused across other templates.
  - **configmap.yaml**: Kubernetes ConfigMap resource definition.
  - **deployment.yaml**: Kubernetes Deployment resource definition.
  - **hpa.yaml**: Kubernetes Horizontal Pod Autoscaler (HPA) configuration.
  - **ingress.yaml**: Kubernetes Ingress resource definition.
  - **networkpolicy.yaml**: Kubernetes NetworkPolicy resource definition.
  - **service.yaml**: Kubernetes Service resource definition.
  - **serviceaccount.yaml**: Kubernetes ServiceAccount resource definition.
