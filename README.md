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

**EC2 Setup and Airflow Installation Commands**
sudo apt update
sudo apt install python3-pip
sudo apt install python3.10-venv
python3 -m venv customer_churn_youtube_venv
source customer_churn_youtube_venv/bin/activate 
sudo pip install apache-airflow
pip install apache-airflow-providers-amazon
airflow standalone

**Redshift Query Editor Database Creation**
CREATE TABLE IF NOT EXISTS customer_churn(
   CustomerID VARCHAR(255),
   City VARCHAR(255),
   Zip_Code INTEGER,
   Gender VARCHAR(255), 
   Senior_Citizen VARCHAR(255),
   Partner VARCHAR(255),
   Dependents VARCHAR(255), 
   Tenure_Months INTEGER,
   Phone_Service VARCHAR(255),
   Multiple_Lines VARCHAR(255),
   Internet_Service VARCHAR(255),
   Online_Security VARCHAR(255),
   Online_Backup VARCHAR(255), 
   Device_Protection VARCHAR(255),
   Tech_Support VARCHAR(255),
   Streaming_TV VARCHAR(255),
   Streaming_Movies VARCHAR(255),
   Contract VARCHAR(255),
   Paperless_Billing VARCHAR(255),
   Payment_Method VARCHAR(255),
   monthly_charges FLOAT,
   Total_Charges FLOAT,
   Churn_Label VARCHAR(255),
   Churn_Value INTEGER,
   Churn_Score INTEGER,
   Churn_Reason TEXT
)
![image](https://github.com/user-attachments/assets/18b4cfc4-d058-4a45-a437-45e8613b2186)


