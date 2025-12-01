# Teleport CE – Installation & Configuration
Teleport Community Edition provides secure access to SSH, Kubernetes, and web apps.\
\
**Installation**
1. Download the Teleport CE package for your distro.
2. Install the package, for example (RPM based):
bash
```
sudo rpm -i teleport.rpm
```
**Configuration**
1. Edit teleport.yaml to configure:
- Auth server and proxies
- SSH/Kubernetes/app access
- Storage backend and certificates
2. Start Teleport and create users/logins.
3. Configure RBAC roles and labels.
4. Join nodes to the cluster using tsh or node configuration.
