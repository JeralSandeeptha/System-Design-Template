# Storage

```js
Total Storage = Data count × Size per data × Retention period
```

<br />

### Example

Assume:
- 1 million users
- Each user stores 2 KB/day
- Data retained for 2 years

```js
2 KB × 365 × 2 × 1,000,000
= 1.46 TB
```

Add overhead

Indexes + metadata ≈ 30–50% extra

➡ Final ≈ 2 TB