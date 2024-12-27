## Backup angular microservice
```
$ velero backup create poc-k8s-keycloak-angular-chart-backup --selector app.kubernetes.io/name=poc-k8s-keycloak-angular-chart
```

## Restore angular microservice
```
$ velero restore create --from-backup poc-k8s-keycloak-angular-chart-backup
```