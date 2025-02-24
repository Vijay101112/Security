AWS Lambda: Sales Analysis Report Automation
Overview
This document provides step-by-step instructions for deploying an AWS Lambda function that automates a sales analysis report by pulling data from an EC2-hosted MySQL database and emailing the results via Amazon SNS. It also covers troubleshooting inbound rules and configuring cron expressions for scheduled execution.

1. Architecture Overview
Components:
AWS Lambda Functions:
salesAnalysisReport: Calls another Lambda function and sends reports.
salesAnalysisReportDataExtractor: Extracts data from a MySQL database.
Amazon EC2: Hosts the MySQL database (LAMP stack).
Amazon SNS: Sends the report via email.
Amazon CloudWatch: Schedules the function using a cron expression.