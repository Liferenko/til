# Donno the pid?

Need to kill process but donno the pid?

```bash
pidof %app_name
```

Too many processes sit on one port? Wanna kill them all? 

```bash
sudo fuser -k %PORT%/tcp
```
