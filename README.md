# argo

🐙 GitOps for Homelab Kubernetes Cluster

## Setup

This argo repository follows an [app of apps](https://argo-cd.readthedocs.io/en/stable/operator-manual/cluster-bootstrapping/) pattern, bootstrapped by the helm chart `inventory/`.

## Structure

```
.
├── apps
│   └── <project>
│       └── <application>
├── install
├── inventory
│   └── values.yaml
└── script
```

### `apps`

These are where all the argo applications are stored, organized by the directory structure, following the pattern `apps/<project>/<application>`. The argo CRDs for `AppProject` and `Application` will be automatically generate by the `inventory/` bootstrap app.