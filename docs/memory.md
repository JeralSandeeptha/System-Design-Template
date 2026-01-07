# Memory / RAM

RAM is just memory used by things that stay in memory at the same time.

<br />
<br />

What uses RAM?
- Application runtime
- Thread pools
- DB connection pool
- Small caches

<br />
<br />

Every backend server has 4 fixed memory buckets:

## Application code & runtime
Your code + framework (Spring Boot / Node / Express)
- Java JAR / Node app
- Loaded classes
- Configs
- Dependency libraries

🧠 From real systems:
- Spring Boot: 300–500 MB
- Node.js: 150–300 MB

👉 We assume ~400 MB

This is NOT guessed — it’s based on typical prod memory usage.

<br />

## Runtime overhead (JVM / Node engine)

The language runtime itself:
- JVM metadata
- Garbage collector structures
- JIT compiler (Java)
- Event loop + heap mgmt (Node)

Typical:
- JVM overhead: 200–400 MB
- Node overhead: 100–200 MB

👉 We assume ~300 MB

<br />

## Thread pools & DB connections
Even if idle, these stay in RAM.

Example:
- 200 threads
- Each thread ~1 MB stack
```cmd
200 × 1 MB = 200 MB
```

DB pool:
- 50 connections
- ~1–2 MB each
```cmd
50 × 2 MB = 100 MB
```

<br />

## Cache (intentional RAM usage)

Example:
- Cache recent URLs
- Cache auth/session data

Then we decide:
```cmd
Let’s allow ~500 MB
```

Why?
- Big enough to matter
- Small enough to not crash the app

This is a design choice, not a formula.

<br />

## OS & buffers (often forgotten!)

Linux needs RAM for:
- File buffers
- Network buffers
- TCP queues
- Kernel operations

Rule of thumb:
- 20–30% of total RAM

If total ≈ 2 GB:
```cmd
~300–400 MB
```

Add them like buckets 🪣
| Bucket           | RAM    |
| ---------------- | ------ |
| App code         | 400 MB |
| Runtime overhead | 300 MB |
| Threads + DB     | 200 MB |
| Cache            | 500 MB |
| OS               | 300 MB |
```cmd
400 + 300 + 200 + 500 + 300
= 1,700 MB ≈ 1.7 GB
```

<br />

Round UP (always!)
- We never deploy exact numbers.

So:
👉 2 GB RAM minimum

In production:
👉 4 GB RAM (cheap, safe, flexible)

<br />

Why 4 GB is commonly chosen

Because:
- RAM is cheap
- Prevents OOM crashes
- Allows future features
- Makes GC smoother

That’s why you see:
```cmd
2 vCPU
4 GB RAM
```
everywhere.

<br />

Important truth (remember this)
-❗ No one expects you to “calculate” RAM exactly
-❗ They expect you to reason about what uses memory

<br />

Ultra-simple memory rule (memorize this)
| Type           | RAM   |
| -------------- | ----- |
| Small service  | 2 GB  |
| Medium service | 4 GB  |
| Heavy service  | 8+ GB |
