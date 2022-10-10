Instructions

$ kind create cluster --config mgmt-cluster-config.yaml
$ clusterctl init --infrastructure docker
$ kubectl apply -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml


$ clusterctl generate cluster c1 --flavor development \
  --infrastructure docker \
  --kubernetes-version v1.25.2 \
  --control-plane-machine-count=3 \
  --worker-machine-count=3 \
  > c1-clusterapi.yaml