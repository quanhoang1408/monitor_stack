Docker needs write permission to `prometheus_data` and `postgres_data`
```
chown -R <user>:<user> prometheus_data
chmod -R 777 prometheus_data
```

To avoid permisison issues:
```
MY_UID="$(id -u)" MY_GID="$(id -g)" docker-compose up -d
```

Ignore `*_data` folders