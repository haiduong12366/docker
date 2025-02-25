<h1>Introduce</h1>
This project is focused on building a data lakehouse, which will help organizations store, manage, and analyze large amounts of data in an affordable, secure, and scalable way. The data lakehouse will act as a central storage space for all data, making it easy for users to access and query data from one place.</br>
</br>
Minio will handle data storage, Delta Lake will manage data changes to ensure reliability, Spark will process large datasets for analysis, and Presto will enable fast SQL queries with Hive Metastore acting as a bridge. Finally, Superset will provide data visualization. This data lakehouse setup will make it easier for organizations to quickly access and analyze important data, supporting better data-driven decision-making.

<h1>DataLake House</h1>

<h2>System Architecture</h2>
<img src="https://github.com/user-attachments/assets/8abeb6ec-8cc7-421e-8e8c-24fdccab0d45"/>
</br>
<B>Bronze Layer</B>: This is raw data collected from websites that has not yet been processed.</br>
</br>
<B>Silver Layer</B>: Here, the data is cleaned and prepared for analysis, making it ready to support business requirements.</br>
</br>
<B>Gold Layer</B>: In this layer, data is reorganized in a warehouse model, making it more convenient for analysis and future machine learning model training.</br>

<h2>Workflow</h2>

1. Data has been crawled from web, will become a Json and import to Minio with spark and delta lake working as layer, data from CSV will be imported to Mysql and streaming data to Broze in Minio.

2. Data will be processed in Minio

3. Presto work as Sql engine to sql processed data.

4. Superset will connect with presto to get sql result to visualize  
 
