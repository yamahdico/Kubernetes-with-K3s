```bash
kubectl apply -f mysql-deployment.yaml
kubectl apply -f php-deployment.yaml
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.13.0/cert-manager.yaml
kubectl apply -f cluster-issuer.yaml
kubectl apply -f php-ingress.yaml
```
