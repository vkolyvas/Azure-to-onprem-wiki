# Kubernetes (Upstream) – Installation & Configuration
Upstream Kubernetes cluster using kubeadm.\

**Installation (Control Plane)**
1. Install container runtime (e.g., containerd) and configure systemd cgroup driver.

2. Install Kubernetes packages (kubeadm, kubelet, kubectl) from the official repo.

3. Initialize the control plane:

bash
```
sudo kubeadm init --pod-network-cidr=<cidr>
```
4. Configure kubectl for the admin user:

bash
```
mkdir -p $HOME/.kube
sudo cp /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```
Join Worker Nodes\
Run the ```kubeadm join``` command printed by ```kubeadm init``` on each worker:

bash
```
sudo kubeadm join <control-plane-ip>:6443 --token <token> --discovery-token-ca-cert-hash <hash>
```
**Cluster Configuration**
- Deploy a CNI plugin (Calico, Flannel, Cilium, etc.).

- Deploy an Ingress controller (e.g., NGINX Ingress).

- Define RBAC roles and role bindings for users and service accounts.

- Deploy the metrics-server and enable resource metrics.
