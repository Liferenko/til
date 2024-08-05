## Which ports are open?

`nmap -Pn %host_ip%`

output example:
```
nmap -Pn 195.***.***.***
Starting Nmap 7.95 ( https://nmap.org ) at 2024-08-01 10:28 CEST
Nmap scan report for 195.***.***.***
Host is up (0.0011s latency).
Not shown: 999 filtered tcp ports (no-response)
PORT   STATE SERVICE
53/tcp open  domain

Nmap done: 1 IP address (1 host up) scanned in 46.27 seconds

```

Useful flags:
- `-sP --traceroute`

