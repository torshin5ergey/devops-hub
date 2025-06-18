## Kubernetes Deploy

- Deploy to cluster
```bash
cd database/clickhouse/
kubectl apply -f k8s/
```
- Test connect with clickhouse-client pod
```bash
kubectl exec -it clickhouse-client -n clickhouse -- bash
```

- Delete
```bash
kubectl delete ns clickhouse
```

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
