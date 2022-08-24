
```bash
helm repo list

helm repo add bitnami https://charts.bitnami.com/bitnami

# Searching a Chart Repository
helm search repo drupal

helm search repo content

helm search repo drupal --versions

```

## installing a Package
```bash
helm install mysite bitnami/drupal
```