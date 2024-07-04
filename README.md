**Automated ETL Pipeline with AWS and Airflow**

**Project Overview**
In this project, I developed an automated ETL pipeline using Amazon Web Services (AWS) and Apache Airflow. The pipeline extracts data from Amazon S3, transforms it using AWS Glue, loads it into Amazon Redshift, and finally visualizes the data in PowerBI. This setup ensures a scalable, efficient, and automated workflow for data processing and analysis.

**Project Details**

1. EC2 Instance Setup:
Created and configured an Amazon EC2 instance to host Apache Airflow.
Installed Python, virtual environments, and Airflow to manage and schedule ETL tasks.

2.Airflow Configuration:
Set up Airflow to run as a web server and scheduler on the EC2 instance.
Configured security settings and connections to allow remote access and interaction through Visual Studio Code.

3. Data Storage in S3:
Created an Amazon S3 bucket to store raw data files.
Uploaded dataset-1 to the S3 bucket and prepared it for crawling and transformation.

4 Redshift Cluster Setup:
Provisioned an Amazon Redshift cluster for data warehousing.
Used the Redshift Query Editor to create a database, rename columns for clarity, and adjust data types for consistency.

5. AWS Glue Configuration:
Established connections between AWS Glue and Redshift.
Created and ran crawlers to catalog the data stored in S3.
Designed Glue ETL jobs to transform the data schema and load it into Redshift.

6. Airflow DAGs for ETL Automation:
Defined a DAG in Airflow to automate the ETL process.
Tasks included triggering Glue jobs, retrieving job run IDs, and monitoring job status using GlueJobSensor.
Configured AWS connections within Airflow to facilitate communication between services.

7. Data Visualization in PowerBI:
Connected PowerBI to the Redshift cluster.
Imported transformed data and created an interactive dashboard to visualize key metrics and insights.

**Technologies Used**
1. Amazon Web Services (AWS): EC2, S3, Glue, Redshift
2. Apache Airflow: For orchestrating and scheduling ETL tasks
3. Python: Scripting and Airflow DAG definitions
3. Visual Studio Code: Remote development and configuration
4. PowerBI: Data visualization and dashboard creation

**Key Achievements**

1. Automation: Automated the entire ETL process from data extraction to visualization, reducing manual intervention and increasing efficiency.
2. Scalability: Leveraged AWS services to create a scalable and robust data pipeline capable of handling large datasets.
3. Data Transformation: Implemented data transformations to ensure consistency and usability of data in the data warehouse.
4. Visualization: Created interactive dashboards in PowerBI to provide meaningful insights and facilitate data-driven decision-making.
   
This project demonstrates my ability to design and implement automated ETL pipelines using cloud services and modern data engineering tools. It showcases my skills in cloud computing, data transformation, and visualization, contributing to efficient and effective data management solutions.




