# 00 — Overview: Delta Lake & Why Optimizations Matter

## What is Delta Lake?
Delta Lake is a **storage layer** on top of Parquet that adds:
- **ACID transactions**
- **Schema enforcement & evolution**
- **Time travel**
- **Concurrency support**

Tables are stored as a collection of Parquet files plus a `_delta_log` folder with JSON transaction logs.

## Why Optimizations Matter
As tables grow, performance can degrade due to:
- Many small files (from micro-batches or streaming).
- Poor partitioning or skewed data distribution.
- Old snapshots taking up storage and slowing queries.

### Core Maintenance Techniques
- **OPTIMIZE**: Compact small files into fewer, larger files.
- **V-Order** (Fabric): Reorders Parquet data to improve scan performance.
- **Z-Order**: Co-locates rows with similar column values to minimize IO for filtered queries.
- **VACUUM**: Permanently removes old files beyond retention period.
- **Time Travel**: Query previous table versions for auditing or rollback.

> In Fabric, V-Order is disabled by default and can be enabled during `OPTIMIZE` or set at the table level.
