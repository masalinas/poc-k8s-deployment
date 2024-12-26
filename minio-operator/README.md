# Description
Deploy minio operator

## Steps

- **STEP01**: Install minio operator:

Install minio operator version 5.0.16 includind the minio console to create and manage tenants:
```
helm install avib-minio-operator --namespace minio-operator --create-namespace minio-operator/operator --version 5.0.16
```