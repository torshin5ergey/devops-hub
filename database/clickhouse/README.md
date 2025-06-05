# ClickHouse

Basic ClickHouse local install.

## References

- https://clickhouse.com/docs/install

## RedHat (AlmaLinux)

1. Add RPM repository
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://packages.clickhouse.com/rpm/clickhouse.repo
```

2. Install ClickHouse server and client
```bash
sudo yum install -y clickhouse-server clickhouse-client

# specified version
sudo yum install -y clickhouse-server-22.8.7.34
```

3. Start ClickHouse server
```bash
sudo systemctl enable clickhouse-server
sudo systemctl start clickhouse-server
sudo systemctl status clickhouse-server
```

4. Connect via client
```bash
clickhouse-client
```
