# Learning Kubernetes with K3s: Insights and Experiences

This repository serves as a comprehensive guide for learning Kubernetes using K3s. Drawing from my hands-on experience, it covers essential concepts, best practices, and real-world scenarios tailored for educators and developers. The content is designed to simplify Kubernetes for learners, offering step-by-step tutorials, code snippets, and troubleshooting techniques.

Key Features:

   - Beginner-Friendly Tutorials: Learn K3s installation, configuration, and cluster management.
   - Advanced Use Cases: Explore load balancing, storage, and multi-node setups.
   - Best Practices: Practical tips for optimizing performance and ensuring security.
   - Interactive Learning: Examples and exercises to apply concepts in real projects.
   - Resources: Links to tools, official documentation, and community guides.

This repository is perfect for anyone looking to understand Kubernetes while benefiting from the lightweight, developer-friendly features of K3s. Whether you’re an educator seeking structured lessons or a developer experimenting with container orchestration, this resource is designed for you.


## kubectl alias k completion

```bash 
echo 'alias k=kubectl' >>~/.bashrc (add alias to shell)
echo 'source <(kubectl completion bash)' >>~/.bashrc (add completion)
echo 'complete -F __start_kubectl k' >>~/.bashrc (make them work together)
```
## Installed PHP modules 
```bash 
kubectl exec -it <php-pod-name> -- php -m
```


## Docker vs CRIctl
```bash 
crictl ps
docker ps
```

## kubectl alias k completion
```bash 
kubectl apply -f mysql-deployment.yaml
kubectl apply -f php-deployment.yaml
kubectl apply -f php-ingress.yaml
```

