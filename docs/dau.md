# Daily Active Users

`DAU` = `Number of unique users` who perform at least one meaningful action in 24 hours.

<br />

### Why DAU matters
- Indicates daily engagement
- Used for capacity planning
- Strong signal for product health

<br />

### Design Implications
- `Peak vs. Average`: Typically 2-3x higher during peak hours
- `Geographic Patterns`: Timezone-based traffic spikes
- `Feature Usage`: Not all DAUs use all features equally
- `Growth Projection`: Usually follows hockey-stick curve in successful products

<br />

### Example
If:
- 1,000,000 registered users
- 120,000 users used the app today
 
➡ DAU = 120k

<br />

### Calculate
```js
DAU = Total Registered Users × Daily Engagement Rate

If 10M registered users with 20% daily engagement → 2M DAU
```