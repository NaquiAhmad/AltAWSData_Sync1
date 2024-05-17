# AltAWSData_Sync1
Building a Scalable Big Data Solution on  AWS Cloud

Environment Variables:

Load the AWS credentials from the .env file using dotenv.
boto3 Client Initialization:

Initialize boto3 clients for DataSync and CloudWatch using the credentials from the environment variables.
DataSync Task Setup and Execution:

Functions for creating locations, tasks, starting the task execution, and monitoring the task status are provided.
CloudWatch metrics are sent to monitor the task status.
PySpark Integration:

After the data synchronization is complete, a PySpark session is started.
The CSV files are read from the S3 bucket using the S3 URL (s3a:// prefix).
Data transformations are performed using PySpark (e.g., filtering out rows where the "city" column is null).
The transformed data is written back to another location in the S3 bucket.
Scheduling:

The schedule library is used to run the sync_data function daily at 2 AM.
The script runs indefinitely to maintain the schedule.
Step 4: Running the Script
    - Open Terminal in VSCode.
    - Provide all integration details.
    - Run the script.
