## Backup angular microservice
This command backup all kubernetes resources and the helm chart secret attached to these resources
```
$ velero backup create poc-k8s-keycloak-angular-chart --or-selector "app.kubernetes.io/name=poc-k8s-keycloak-angular-chart or name=poc-k8s-keycloak-angular"
```

## Restore angular microservice
```
$ velero restore create --from-backup poc-k8s-keycloak-angular-chart
```