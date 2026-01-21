# UI for Spark Declarative Pipeline (SDP)

Published VS Code extension to visualize Apache Spark Declarative Pipeline (SDP) YAML files.


![Screenshot](media/screenshot_2.png)

## Features
- Visualize pipeline DAGs from YAML, Python, and SQL files
- Click nodes to open source code directly in editor
- Preview code snippets with syntax highlighting in sidebar
- Live updates on file save

## Entity Definition Syntax

The SDP parser recognizes entities defined using the `@dp.` or `@sdp.` decorator syntax in Python files. Entities must be decorated with one of the following patterns:

### Supported Decorators

| Decorator | Entity Type |
|-----------|-------------|
| `@dp.table(name="...")` | Table |
| `@dp.view(name="...")` | View |
| `@dp.materialized_view(name="...")` | Materialized View |
| `@dp.temporary_view(name="...")` | Temporary View |
| `@dp.streaming_table(name="...")` | Streaming Table |

### Example

```python
from pyspark.sql import SparkSession
from pyspark import pipelines as dp  # or sdp

@dp.materialized_view(name="sales_summary")
def create_sales_summary(spark: SparkSession):
    return spark.sql("""
        SELECT region, SUM(amount) as total
        FROM raw_sales
        GROUP BY region
    """)

@dp.table(name="customers_enriched")
def enrich_customers(spark: SparkSession):
    return spark.sql("""
        SELECT c.*, o.order_count
        FROM raw_customers c
        LEFT JOIN order_counts o ON c.id = o.customer_id
    """)
```

> **Note:** The parser extracts the `name` parameter from the decorator to identify entities and their dependencies in SQL queries.

## Usage
1. Open a workspace containing a `pipeline.yml`, Python, or SQL pipeline file.
2. Click the SDP Pipeline Visualizer icon in the Activity Bar.
3. Select a pipeline from the automatically listed files in the sidebar.
4. View the pipeline DAG and entity details in the sidebar and webview.

## Installation
You can install the extension from the VSIX package or the VS Code Marketplace (if published there).

### From VSIX
1. Download the latest `.vsix` file from the releases or build it locally.
2. In VS Code, run `Extensions: Install from VSIX...` and select the file.

### From Marketplace
1. Search for "UI for Spark Declarative Pipeline" in the Extensions view.
2. Click Install.


## Usage
1. Open a workspace containing a `pipeline.yml`, Python, or SQL pipeline file.
2. Click the SDP Pipeline Visualizer icon in the Activity Bar.
3. Select a pipeline from the automatically listed files in the sidebar.
4. View the pipeline DAG and entity details in the sidebar and webview.

## Developer

Developed by Gergely Szécsényi

## License
BSD 2-Clause License — see LICENSE for details.

