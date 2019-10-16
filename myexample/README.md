# Helm Chart MyExample

## Prerequisite
To use the template you need the following components :
* Kubernetes Cluster
* Ingress Controller Nginx
* Helm client/server
* DNS Zone (example ilab.team)
* (optional) CertManager for https

# Before starting
To disable CertManager you need to comment the following line in `values.yaml`:
```yaml
ingress:
    ...
    # kubernetes.io/tls-acme: "true"
```

## Getting started
Deploy the application on the cluster in the namespace `myexample`.
```
helm install --name=myexample --namespace=myexample -f values.yaml .
```

Go at the URL :
* https://myexample.kube.ilab.team
* https://myexample-api.kube.ilab.team/
