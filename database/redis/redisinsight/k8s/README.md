# Redis Insight Kubernetes Deploy

- Deploy to cluster
```bash
cd database/redis/redisinsight/
kubectl apply -f k8s/
```
- Port forward
```bash
kubectl -n redisinsight port-forward deployment/redisinsight 5540:5540
```
- Access with web browser `http://localhost:5540`

- Delete
```bash
kubectl delete ns redisinsight
```

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
