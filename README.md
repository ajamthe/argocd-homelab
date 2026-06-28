# argocd-homelab

GitOps source of truth for my homelab (k3s on lancelot), managed by Argo CD.

**The rule:** I do not `kubectl apply` to this cluster. I change YAML here, commit, and
Argo CD reconciles the cluster to match. Git is the source of truth.

- `web/` — a simple nginx app, deployed by Argo CD with automated sync + self-heal.
