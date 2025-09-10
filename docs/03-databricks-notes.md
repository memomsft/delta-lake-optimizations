# 03 — Databricks Notes

- `OPTIMIZE`, `ZORDER BY`, and `VACUUM` commands work the same way in Databricks.
- `V-Order` is Fabric-specific; in Databricks focus on Z-Order + Optimize Write.
- Default `VACUUM` retention is 7 days.
- Time Travel by `VERSION AS OF` or `TIMESTAMP AS OF` works identically.
