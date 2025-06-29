# gitlab-runner-k8s-deploy

use command below to deploy gitlab runner on k8s with helm
helm repo add gitlab https://charts.gitlab.io/
helm repo update
helm install gitlab-runner gitlab/gitlab-runner   --namespace gitlab-runner   --create-namespace   -f values.yaml

for upgrading you can use below command
helm upgrade gitlab-runner gitlab/gitlab-runner   --namespace gitlab-runner   -f values-new-final.yaml 
