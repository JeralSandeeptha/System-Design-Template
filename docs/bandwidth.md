# Network Bandwidth

Amount of data transferred per second

```js
Bandwidth = Throughput × (request + response size)
```

Example 
- Req = 5 KB
- Res = 50 KB
- RPS = 500
```js
Total = 55 KB × 500 = 27.5 MB/sec
```

➡ Need at least 220 Mbps (plus buffer)

<br />
<br />
<br />

Components:
- `North-South`: Client to server traffic
- `East-West`: Inter-server communication (microservices, database replication)
- `CDN Traffic`: Often 80-90% of total bandwidth for content-heavy apps

Cost Implications:
- Data transfer costs can dominate cloud bills
- Geographic distribution reduces cross-region costs

<br />
<br />
<br />

Bandwidth has 2 types 
- Inbound Bandwidth (Ingress)
- Outbound Bandwidth (Egress)

<br />
  
### Inbound Bandwidth (Ingress)

How many data write / comes into our system from outsid

```js
Ingress Bandwidth = write throughput / day per second
```

<br />

### Outbound Bandwidth (Egress)

How many data read / goes to outside from our system.

```js
Ingress Bandwidth = read data * size of a data  / day per second
```