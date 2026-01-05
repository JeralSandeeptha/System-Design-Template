# Traffic & Load

Traffic / Load has two varients
- [Server Traffic](./server_traffic.md)
- [Database Traffic](./db_traffic.md)

<br />

When we are working with these types of traffics, first we need to assume and we want the users count which is the number of users interact with our system.

These traffics are depending on the `DAU` and `MAU`. We can measure them by [`DAU`](./dau.md) and [`MAU`](./mau.md).

<br />

If you are know `DAU` and `MAU` you are good to go calculate traffic speed.

There are 2 types of traffic speed
- `RPS - Requests Per Second` - Number of HTTP/API requests your system receives per second
- `QPS – Queries Per Second` - Number of database queries per second

Makesure,
`RPS ≥ QPS? ❌
Usually QPS > RPS because one request can trigger multiple DB queries.`

<br />
<br />

### Calculate RPS

Assume:
- DAU = 100,000
- Avg requests per user per day = 50

```js
Total requests/day = 100,000 × 50 = 5,000,000
Average RPS = 5,000,000 / 86,400 ≈ 58 RPS
```

Peak traffic rule:
- Peak traffic ≈ 5–10× average
```js
Peak RPS ≈ 300–600
Peak Factor typically 2-5x average
```

<br />
<br />

### Calculate QPS

If:
- Each request causes 4 DB queries

```js
QPS = RPS × queries/request
QPS = 500 × 4 = 2000 QPS
```