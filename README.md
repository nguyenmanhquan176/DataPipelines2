# Project Title: 
Project: Data Pipelines

# Description: 
To create custom operators to perform tasks such as staging the data, filling the data warehouse and running checks on the data as the final step. We have been provided with four empty operators that need to be implemented into functional pieces of a data pipeline.

# Stage Operator
The stage operator is expected to be able to load any JSON and CSV formatted files from S3 to Amazon Redshift. The operator creates and runs a SQL COPY statement based on the parameters provided. The operator's parameters should specify where in S3 the file is loaded and what is the target table.

# Fact and Dimension Operators
Provided SQL Helper class will help to run data transformations. Most of the logic is within the SQL transformations and the operator is expected to take as input a SQL statement and target database on which to run the query against. Dimension loads are often done with the truncate-insert pattern where the target table is emptied before the load. Fact tables are usually so massive that they should only allow append type functionality.

# Data Quality Operator
The final operator to create is the data quality operator, which is used to run checks on the data itself. The operator's main functionality is to receive one or more SQL based test cases along with the expected results and execute the tests. For each the test, the test result and expected result needs to be checked and if there is no match, the operator should raise an exception and the task should retry and fail eventually.

# Executing
When you are in the workspace, after completing the code, you can start by using the command : /opt/airflow/start.sh
Once you done, it would automatically start all the dags required and outputting the result to its respective tables

# Authors
Contributors names and contact info

ex. Nguyen Manh Quan
ex. @NguyenManhQuan

 python create_redshift_cluster.py --query_file create_tables.sql
!python create_tables.py