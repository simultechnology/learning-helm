
```bash
helm install wordpress bitnami/wordpress

helm upgrade wordpress bitnami/wordpress --set image.pullPolicy=NoSuchPolicy

helm get notes wordpress

helm get values wordpress

helm upgrade wordpress bitnami/wordpress --set image.tag=latest

helm get values wordpress --revision 4

helm get values wordpress --all

# This returns the manifest generated from the template
helm get manifest wordpress

# This returns the current state of all of your resources
kubectl get secret wordpress-mariadb -o yaml

helm history wordpress

helm rollback wordpress 2
```

```bash
helm install bitnami/wordpress --generate-name

# if namespace doesn't exist, it will be created
helm install drupal bitnami/drupal --namespace mynamespace --create-namespace
# if 
helm upgrade --install my-wordpress bitnami/wordpress --namespace test --create-namespace
```

```bash 
helm install --wait 
```
is a good tool for making sure that the release is brought all the way to running. 

```bash 
helm install --atomic
```
This flag causes the same behavior as --wait unless the release fails. Then, instead of marking the release as failed and exiting, it performs an automatic rollback to the last successful release.


Thus, it is recommended to use longer --timeout durations for --atomic, especially when used with CI systems.