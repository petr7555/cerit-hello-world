From tutorial http://docs.cerit.io/docs/kubectl-helloworld.html.

# Deploy:
- `kubectl --kubeconfig kuba-cluster.yaml apply -f hello-kubernetes -n janik-ns`
- check status:
  - pods: `kubectl --kubeconfig kuba-cluster.yaml get pods -n janik-ns`
  - services: `kubectl --kubeconfig kuba-cluster.yaml get services -n janik-ns`
  - ingress: `kubectl --kubeconfig kuba-cluster.yaml get ingress -n janik-ns`
- visit [https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/](https://hello-kubernetes-petr7555.dyn.cloud.e-infra.cz/)

