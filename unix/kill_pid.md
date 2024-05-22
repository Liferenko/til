# When port is busy

how to get a port owner PID & kill thy process

```
kill -9 $(lsof -t -i :5432) ; docker compose up -d
```
