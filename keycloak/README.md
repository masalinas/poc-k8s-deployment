## Backup Keycloak
```
$ velero backup create keycloak-backup --selector app.kubernetes.io/name=keycloak
```

## Restore Keycloak
```
$ velero restore create --from-backup keycloak-backup
```