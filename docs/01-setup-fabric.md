# 01 — Setup in Microsoft Fabric (UI)

All steps are done through the UI — no CLI is required.

## 1. Create a Workspace
Go to **Fabric Home → Workspaces → +New workspace**  

## 2. Create a Lakehouse
Go to your new Workspace **Workspace → New item → Search for Lakehouse → Create**  

Name it `lakehouse_opt_lab`.

## 3. Create a Notebook
Inside the Lakehouse, click **New Notebook**.  
Set the default language to **PySpark**.

## 4. Attach & Run
Attach the notebook to the Lakehouse (top-left).  
Test with a simple cell:

```python
spark.range(1, 3).show()
```

If you see output with numbers 0, 1, 2 — your cluster is working and ready.
