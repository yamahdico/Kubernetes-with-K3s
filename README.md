# k3s


# kubectl alias k 

  echo 'alias k=kubectl' >>~/.bashrc (add alias to shell)

  echo 'source <(kubectl completion bash)' >>~/.bashrc (add completion)

  echo 'complete -F __start_kubectl k' >>~/.bashrc (make them work together)
