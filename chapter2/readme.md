

```bash

helm repo add bitnami https://charts.bitnami.com/bitnami

helm repo list

# Searching a Chart Repository
helm search repo drupal

helm search repo content

helm search repo drupal --versions

```

## installing a Package
```bash
helm install mysite bitnami/drupal
```

## others
```bash
helm repo update
```