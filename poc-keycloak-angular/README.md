## Backup angular microservice
using selector
```
$ velero backup create poc-k8s-keycloak-angular-chart-backup --selector app.kubernetes.io/name=poc-k8s-keycloak-angular-chart
```

using release
```
$ velero backup create poc-k8s-keycloak-angular-chart-backup --selector release=poc-k8s-keycloak-angular
```
## Restore angular microservice
```
$ velero restore create --from-backup poc-k8s-keycloak-angular-chart-backup
```