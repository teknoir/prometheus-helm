# Prometheus Helm Chart

This chart deploys the Prometheus to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the Prometheus to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: prometheus
  namespace: default
spec:
  repo: https://teknoir.github.io/prometheus-helm
  chart: prometheus
  targetNamespace: default
  valuesContent: |-
    # TBD
```

## Example values.yaml

```yaml
# TBD
```

## Adding the repository

```bash
helm repo add teknoir-prometheus https://teknoir.github.io/prometheus-helm/
```

## Installing the chart

```bash
helm install prometheus teknoir-prometheus/prometheus -f values.yaml
```