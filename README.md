# krew-index

Custom [Krew](https://krew.sigs.k8s.io/) index for my kubectl plugins.

```sh
kubectl krew index add danilazanin https://github.com/DanilaZanin/krew-index.git
kubectl krew install danilazanin/whydied
kubectl krew install danilazanin/unstick
```

| Plugin | Command | What it does |
|---|---|---|
| [whydied](https://github.com/DanilaZanin/kubectl-whydied) | `kubectl whydied POD` | Explains why a container or pod died or restarted, with evidence for every claim |
| [unstick](https://github.com/DanilaZanin/helm-unstick) | `kubectl unstick scan -A` | Recovers Helm releases stuck in a pending state |

Each manifest points at a GitHub release archive and pins its sha256. CI installs both plugins from this index on Linux and macOS on every push.

Update after a new release: `kubectl krew upgrade`.
