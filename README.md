From tutorial http://docs.cerit.io/docs/kubectl-helloworld.html.

# Deploy:
- `kubectl --kubeconfig kuba-cluster.yaml apply -f hello-kubernetes -n janik-ns`
- check status:
  - pods: `kubectl --kubeconfig kuba-cluster.yaml get pods -n janik-ns`
  - services: `kubectl --kubeconfig kuba-cluster.yaml get services -n janik-ns`
  - ingress: `kubectl --kubeconfig kuba-cluster.yaml get ingress -n janik-ns`
  - persistent volume claim: `kubectl --kubeconfig kuba-cluster.yaml get pvc -n janik-ns`
- visit [https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/](https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/)

# Persistent volume demo:
- find some pod: `kubectl --kubeconfig kuba-cluster.yaml get pods -n janik-ns`
- exec into it: `kubectl --kubeconfig kuba-cluster.yaml exec -it <POD_NAME> -n janik-ns -- /bin/sh`
- create persistent file: `touch /work/file.txt`

# Debug:
- find some pod: `kubectl --kubeconfig kuba-cluster.yaml get pods -n janik-ns`
- show logs: `kubectl --kubeconfig kuba-cluster.yaml logs <POD_NAME> -n janik-ns`
