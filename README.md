# Keycloak Authentication Tutorial (Helm Kubernetes)

This repo contains all the code needed to follow along with our **[YouTube Tutorial](https://youtu.be/YNBCi5tKxUA)**

# ⚠️⚠️⚠️ WARNING

If you're following this tutorial after September 2025, **adjust** the command shown at timestamp 6:22 of the Youtube Video from:

```bash
helm install keycloak bitnami/keycloak --version 24.4.9 -n keycloak --create-namespace -f helm/values.yaml
```

### **to**

```bash
helm install keycloak bitnami/keycloak --version 24.4.9 -n keycloak --create-namespace -f helm/values.yaml --set image.repository=bitnamilegacy/keycloak --set postgresql.image.repository=bitnamilegacy/postgresql --set global.security.allowInsecureImages=true
```

### **Why?**

The bitnami keycloak image is being blocked by a paywall, so using the first command will cause your pods to fail after installing the helm chart. However, the second command installs the same helm chart but pulls the keycloak images from the legacy bitnami repository instead.


## Tutorial Resources
- Set Up Kubernetes Cluster with Docker Desktop: [Kubernetes Cluster Setup](https://youtu.be/IBkU4dghY0Y)
- Install Helm on Mac and Windows: [Install Helm](https://rayanslim.com/course/prometheus-grafana-monitoring-course/helm-installation)
- Helm Repository: [bitnami helm repo](https://charts.bitnami.com/bitnami)
- Postman Download: [Download Postman](https://www.postman.com/downloads/)

## Become a Cloud and DevOps Engineer

Learn every tool that matters: https://rayanslim.com
