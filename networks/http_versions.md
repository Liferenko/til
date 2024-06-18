# HTTP 1.1, 2.0, 3.0

I've fucked up these questions during last interview. So it's better to fresh those knowledges up.

### HTTP 1.1
- Loads resources one by one. If one of requested files is broken - all files after it won't be downloaded. HTTP 2.0 has Multiplexing

```mermaid
  sequenceDiagram
    Host_browser_or_Target_server->>+Application_layer: "HTTP"
    Application_layer-->>+Transport_layer: "TCP"
    Transport_layer->>+Network_layer: "IP"
    Network_layer->>+Data_link_layer: "..."

    Data_link_layer-->>+Network_layer: "..."
    Network_layer-->+Transport_layer: "IP"
    Transport_layer-->+Application_layer: "TCP"
    Application_layer-->+Host_browser_or_Target_server: "HTTP"
```


### HTTP 2.0

Streams added

### HTTP 3.0

QUIC protocol added (UDP based). QUIC is an equivalent to TCP+TLS. 
Best for working with frequent reconnection (wifi -> 5G -> 4G -> Wifi -> another Wifi -> ...)

