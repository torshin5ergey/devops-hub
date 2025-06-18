# Redis Insight

## References

- [Install Redis Insight](https://redis.io/docs/latest/operate/redisinsight/install/)
- [redis/redisinsight Dockerhub](https://hub.docker.com/r/redis/redisinsight)

## Docker Deploy

- Run Docker container
```bash
docker run -d \
  --name redisinsight \
  -p 5540:5540 \
  redis/redisinsight
```
- Access with web browser `http://localhost:5540`

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
