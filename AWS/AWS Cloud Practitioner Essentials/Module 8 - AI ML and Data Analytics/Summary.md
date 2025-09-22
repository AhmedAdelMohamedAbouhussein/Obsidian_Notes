![[Pasted image 20250918233442.png]]

1. An e-commerce company uses an ML model to make product recommendations.
2. An Amazon DynamoDB database stores the historical customer data gathered through the app. This makes sense for low-latency reads and writes but isn't ideal for ML model training.
3. Kinesis Data Streams ingests the data from DynamoDB. Amazon Data Firehose then aggregates the data.
4. The data is in JSON format, so Firehose invokes an AWS Lambda function that transforms the data into .csv format.
5. Firehose then delivers the data to the company's Amazon S3 data lake, where it is available for multiple consumers.
6. AWS Glue Data Catalog serves as a metadata repository with tables that describe the schema and location of the Amazon S3 data.
7. Data scientists use Athena to gather insights through queries.
8. SageMaker AI reads the same dataset directly from Amazon S3. ML engineers can then train new versions of the recommendation model using the latest information


# 📚 AWS AI, ML & Data Analytics – Resources

## 🤖 AI & ML Services

- **[Amazon Comprehend](#)** → Extract key insights from documents using NLP.
    
- **[Amazon Polly](#)** → Convert text into lifelike speech.
    
- **[Amazon Transcribe](#)** → Convert speech into text.
    
- **[Amazon Translate](#)** → Translate text into multiple languages.
    
- **[Amazon Kendra](#)** → NLP-powered enterprise search across content.
    
- **[Amazon Rekognition](#)** → Detect objects, faces, and activities in images & videos.
    
- **[Amazon Textract](#)** → Extract typed & handwritten text from documents.
    
- **[Amazon Lex](#)** → Build conversational interfaces (chatbots, voicebots).
    
- **[Amazon Personalize](#)** → Generate personalized customer recommendations.
    

---

## ⚙️ ML Development Platforms

- **[Amazon SageMaker](#)** → Build, train, and deploy ML models without infrastructure overhead.
    
- **[Amazon SageMaker JumpStart](#)** → One-click deployment of pre-trained ML solutions (CV, NLP, tabular data).
    
- **[Amazon Bedrock](#)** → Integrate and fine-tune foundation models (FMs) via API.
    
- **[Amazon Q Business](#)** → Answer questions using company data repositories.
    
- **[Amazon Q Developer](#)** → Accelerate development with AI-powered code recommendations.
    

---

## 📡 Data Ingestion & Streaming

- **[Amazon Kinesis Data Streams](#)** → Ingest terabytes of streaming data in real time.
    
- **[Amazon Kinesis Data Firehose](#)** → Deliver streaming data to lakes, warehouses, and analytics tools within seconds.
    
- **[Amazon S3](#)** → Scalable data lake for storing virtually unlimited data.
    

---

## 🏗️ Data Warehousing & Processing

- **[Amazon Redshift](#)** → Petabyte-scale data warehouse for structured/semi-structured data with SQL analytics.
    
- **[AWS Glue Data Catalog](#)** → Centralized metadata repository for analytics services.
    
- **[AWS Glue](#)** → ETL and data preparation with Glue Data Catalog integration.
    
- **[Amazon EMR](#)** → Big data processing with frameworks like Apache Spark.
    
- **[Amazon Athena](#)** → Serverless SQL queries across data stored in multiple sources.
    

---

## 📊 Data Visualization & Search

- **[Amazon QuickSight](#)** → Create interactive dashboards with or without data expertise.
    
- **[Amazon OpenSearch Service](#)** → Real-time data analytics, visualization, and keyword/NLP-powered search.