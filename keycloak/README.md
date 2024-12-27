## Some health probes isues
If you have some problems with timeouts in the healtprobes edit the statefulset for the postgreSQL and set a upper time in seconds for the livenessProbe and/or readinessProbe

```
$ kubectl edit statefulset avib-keycloak-postgresql
```

In my case I change these values in both health probes:

```
initialDelaySeconds: 300
timeoutSeconds: 500
```

## Backup Keycloak
```
$ velero backup create keycloak-backup --selector app.kubernetes.io/name=keycloak
```

## Restore Keycloak
```
$ velero restore create --from-backup keycloak-backup
```