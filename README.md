# todo-app-EKS
Deploying To-Do app in EKS Cluster with ArgoCD
Failed to load live state: failed to get cluster info for "https://kubernetes.default.svc": error synchronizing cache state : failed to sync cluster https://10.100.0.1:443: failed to load initial state of resource FlowSchema.flowcontrol.apiserver.k8s.io: failed to list resources: flowschemas.flowcontrol.apiserver.k8s.io is forbidden: User "system:serviceaccount:argocd1:argocd-application-controller" cannot list resource "flowschemas" in API group "flowcontrol.apiserver.k8s.io" at the cluster scope


apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: argocd1-application-controller
roleRef:
  apiGroup: rbac.authorization.k8s.io
  kind: ClusterRole
  name: cluster-admin
subjects:
- kind: ServiceAccount
  name: argocd-application-controller
  namespace: argocd1
