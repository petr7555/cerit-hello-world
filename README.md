From tutorial http://docs.cerit.io/docs/kubectl-helloworld.html.

Kubernetes configuration `kuba-cluster.yaml` was downloaded
from [Rancher](https://rancher.cloud.e-infra.cz/dashboard/c/c-m-qvndqhf6) and default namespace `janik-ns` was added.

- The token in `kuba-cluster.yaml` is no longer valid, and you'll need to download the config file again.

# Deploy:

- `kubectl --kubeconfig kuba-cluster.yaml apply -f hello-kubernetes`
- check status:
	- pods: `kubectl --kubeconfig kuba-cluster.yaml get pods`
	- services: `kubectl --kubeconfig kuba-cluster.yaml get services`
	- ingress: `kubectl --kubeconfig kuba-cluster.yaml get ingress`
	- persistent volume claim: `kubectl --kubeconfig kuba-cluster.yaml get pvc`
- visit
  [https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/](https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/)

# Persistent volume demo:

- find some pod: `kubectl --kubeconfig kuba-cluster.yaml get pods`
- exec into it: `kubectl --kubeconfig kuba-cluster.yaml exec -it <POD_NAME> -- /bin/sh`
- create persistent file: `touch /work/file.txt`

# Debug:

- find some pod: `kubectl --kubeconfig kuba-cluster.yaml get pods`
- show logs: `kubectl --kubeconfig kuba-cluster.yaml logs <POD_NAME>`
