# Add Helm Repo and Update
```
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
```

# Extract values.yaml and change Grafana "true" and version
```
helm show values grafana/loki-stack > values.yaml
```

# Install using values.yaml
```
helm install --values values.yaml loki grafana/loki-stack
```

# Access Grafana UI and get password from secret
