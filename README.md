# gitlab-runner-k8s-deploy

## 🚀 Deploy GitLab Runner on Kubernetes Using Helm

Use the following steps to install and upgrade a GitLab Runner on your Kubernetes cluster with Helm.

---

### 🛠 Step 1: Add GitLab Helm Repository

```bash
helm repo add gitlab https://charts.gitlab.io/
helm repo update
helm install gitlab-runner gitlab/gitlab-runner \
  --namespace gitlab-runner \
  --create-namespace \
  -f values.yaml
helm upgrade gitlab-runner gitlab/gitlab-runner \
  --namespace gitlab-runner \
  -f values-new-final.yaml
