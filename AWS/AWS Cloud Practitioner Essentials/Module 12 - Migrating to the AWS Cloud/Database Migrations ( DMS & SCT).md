**Services to plan, migrate, and, if needed, convert**

Migrating your database to the cloud can provide an opportunity to redesign and improve your database architecture. Because legacy systems and requirements change over time, you might also consider whether to migrate to an AWS managed database service or an open source database to reduce licensing costs. It is fairly simple to migrate data from one server to another when both are using the same database engine, known as homogeneous migration. Going to a different engine, or heterogeneous migration, is more complex and might require changes in your application. The good news is, whether your migration is homogenous (from same type of database to same type) or heterogenous (from one type of database to a different type), there are AWS services to support you.


> **AWS DMS**

The AWS Database Migration Service (AWS DMS) makes it possible to quickly and securely migrate databases and perform ongoing data replication tasks for live databases and data warehouses. It provides a way to plan, assess, convert, and migrate databases even with data warehouses in one central tool.

**Benefits:** AWS DMS provides benefits for migrating databases including maintaining high availability and low downtime during the migration process. It supports homogenous and heterogenous migrations. It also makes it possible to migrate terabyte sized databases at a low cost.

**Use cases:** You can use AWS DMS to move to managed databases, remove licensing costs, replicate ongoing changes in your database, and improve integration with data lakes.





If you want to change from a commercial database to an open source database during your migration, there are a few important logistics. When the databases you are migrating have different source and target engines, you need to consider how to recreate existing resources, like the database schema, in the target. A schema defines the structure and organization of data inside the database and acts like a blueprint for things like table structures, field types, and relationships between items. It can be time consuming to recreate everything manually. That's where AWS Schema Conversion Tool (AWS SCT) can help.

> **AWS SCT**

AWS SCT makes it possible to convert database schemas and code objects (like stored procedures, views, and functions) from one database engine to another. AWS SCT can even give you estimates of how big of an effort a conversion is, which helps with planning.

**Benefits:** AWS SCT provides benefits to simplify database migrations by automating schema analysis, recommendations, and conversion at scale. It is compatible with popular databases and analytics services as source and target engines. It can save weeks or months of manual time and resources, which are typically required in conversions.

**Use cases:** You can use AWS SCT to move from commercial databases to open source databases. You can also use it for migrating large data warehouse workloads and modernizing or updating database schemas in place.