# 01 — Setup in Microsoft Fabric (UI)

All steps are done through the UI — no CLI is required.

## 1. Create a Lakehouse
Go to **Fabric Home → Data Engineering → Lakehouse → Create**  
Name it `lakehouse_opt_lab`.

## 2. Create a Notebook
Inside the Lakehouse, click **New Notebook**.  
Set the default language to **PySpark**.

## 3. Attach & Run
Attach the notebook to the Lakehouse (top-left).  
Test with a simple cell:

```python
spark.range(1, 3).show()
```
