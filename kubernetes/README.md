# Kubernetes Commands and Installation

## Installation

### On Ubuntu
```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF
sudo apt-get update
sudo apt-get install -y kubelet kubeadm kubectl
sudo apt-mark hold kubelet kubeadm kubectl
```

### On CentOS
```bash
cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF
sudo yum install -y kubelet kubeadm kubectl
sudo systemctl enable --now kubelet
```

## Useful Kubernetes Commands

- Check cluster status:
  ```bash
  kubectl cluster-info
  ```

- Get nodes:
  ```bash
  kubectl get nodes
  ```

- Get pods:
  ```bash
  kubectl get pods --all-namespaces
  ```

- Apply a configuration:
  ```bash
  kubectl apply -f <file.yaml>
  ```

- Delete a resource:
  ```bash
  kubectl delete -f <file.yaml>
