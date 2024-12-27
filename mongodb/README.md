## Backup MongoDB
```
$ velero backup create mongodb-backup --selector app.kubernetes.io/name=mongodb
```

## Restore MongoDB
```
$ velero restore create --from-backup mongodb-backup
```