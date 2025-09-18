## 🏗️ **Data Warehouse**

- **Definition**: A **centralized repository** that stores **structured data** (organized in rows/columns, like SQL tables) for reporting and analytics.
    
- **Schema**: **Schema-on-write** → data is cleaned, transformed, and structured before it’s loaded.
    
- **Performance**: Optimized for fast queries (OLAP – Online Analytical Processing).
    
- **Best For**: Business Intelligence (BI), dashboards, trend analysis.
    
- **Examples**:
    
    - Amazon Redshift
        
    - Google BigQuery
        
    - Snowflake
        

---

## 🌊 **Data Lake**

- **Definition**: A **storage repository** that holds **raw data** in its native format (structured, semi-structured, or unstructured).
    
- **Schema**: **Schema-on-read** → data is stored as-is, and structure is applied only when you read/query it.
    
- **Performance**: More flexible, but queries may be slower unless optimized.
    
- **Best For**: Big data analytics, machine learning, real-time streaming.
    
- **Examples**:
    
    - Amazon S3 (as a data lake)
        
    - Azure Data Lake Storage
        
    - Hadoop (HDFS)

![[Pasted image 20250918232304.png]]