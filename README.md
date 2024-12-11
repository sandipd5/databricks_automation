# Azure Data Factory Notebook Scheduling

## Overview
This repository contains an Azure Data Factory (ADF) pipeline that schedules and runs Databricks notebooks. The pipeline dynamically uses parameters to select and execute specific notebooks within a Databricks workspace. This setup allows automated execution of Databricks notebooks as part of a larger ETL or data processing workflow.

## Components
1. **Linked Service**:
   - A Databricks linked service is configured to connect to the Databricks workspace.
   - It includes the necessary authentication and endpoint details.

2. **Pipeline**:
   - A Data Factory pipeline that:
     - **Loads data** from a specified location.
     - **Transforms** the data as per the required business logic.
     - **Schedules** specific Databricks notebooks using dynamic parameters.

3. **Databricks Notebooks**:
   - Multiple Databricks notebooks reside in a specified folder within the Databricks workspace.
   - The pipeline uses dynamic parameters to specify which notebook to run.

## How It Works
1. **Linked Service Configuration**:
   - A Databricks linked service is created to connect to the Databricks workspace.
   - The linked service allows Data Factory to authenticate and interact with Databricks notebooks.

2. **Pipeline Configuration**:
   - The ADF pipeline dynamically selects and runs Databricks notebooks.
   - It uses dynamic parameters to pass information such as the notebook path, workspace name, and any required input parameters.
   - The pipeline can be scheduled to run at specific intervals to maintain data consistency and freshness.

3. **Scheduling**:
   - The notebook execution can be scheduled using Azure Data Factory.
   - The schedule allows for automated execution based on defined triggers.

## Requirements
- **Azure Data Factory**: For orchestrating the workflow.
- **Databricks Workspace**: To house the Databricks notebooks.
- **Git**: To clone the repository and sync changes.


