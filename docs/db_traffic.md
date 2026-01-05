# Database Traffic

Database traffic refers to the amount of activity and data flow between a database and the applications or users that access it.

In simple terms, it means: how often the database is being used and how much data is being read or written.

<br />

### What counts as database traffic
- `Queries` – SELECT, INSERT, UPDATE, DELETE operations
- `Read traffic` – how much data is read from the database
- `Write traffic` – how much data is written or modified
- `Connections` – number of active or total database connections
- `Transactions` – groups of database operations
- `Data transfer` – amount of data sent between the database and app

<br />

### Common ways database traffic is measured
- Queries per second (`QPS`)
- Transactions per second (`TPS`)
- Rows read / rows written
- Active connections
- Data size transferred (`MB`/`GB`)

<br />

### Why database traffic matters
- `Performance`: High traffic can slow queries and increase latency
- `Scalability`: Helps decide when to add read replicas, caching, or sharding
- `Reliability`: Too much traffic can cause timeouts or crashes
- `Cost`: Managed databases often charge based on usage and throughput

<br />

### Difference from web traffic
- `Web traffic` = users hitting your website/app
- `Database traffic` = internal data operations caused by those users