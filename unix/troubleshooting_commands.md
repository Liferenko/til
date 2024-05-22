### Linux troubleshooting

1) [Google SRE books](https://sre.google/books/)

2) Top commands for troubleshooting:
```
- uptime
- dmesg | tail
- vmstat 1
- mpstat -P ALL 1
- pidstat 1
- iostat -xz 1
- free -m
- sar -n DEV 1
- sar -n TCP,ETCP 1
- top
- tcpdump -t
- ss -tulpn \ netstat -tulpn # might be used with watch - will be updated each 2 sec
- iftop
```

3) Performance observabolity tools - [picture](https://miro.medium.com/max/1000/1*nwNScSVlCA8lGl75YdA5hQ.png)

4) [related Netflixtech posts](https://brendangregg.com/linuxperf.html)
